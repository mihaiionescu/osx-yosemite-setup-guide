# Running a Docker Based Environment With Vagrant

The end result will be a development environment which will only require `vagrant up` to setup a complete Docker-based environment. The components of this environment are:
* VM running Linux with Docker installed.
* Separate Docker containers for Rails, PostgreSQL and Redis.
* A shared folder linked to the Docker container so you can carry on editing Rails code on your development machine as you do now, and see those changes instantly reflected on `http://localhost:3000`.
* A simple interface for running all the normal Rails commands (`rake db:migrate`, `rails c` etc) in the Docker environment.

http://www.talkingquickly.co.uk/2014/06/rails-development-environment-with-vagrant-and-docker/

## Docker

### Generalities

##### Useful tutorial links:

* http://blog.flux7.com/blogs/docker/docker-tutorial-series-part-3-automation-is-the-word-using-dockerfile

#### Container vs Image

Images are containers in a certain state. Say you installed ubuntu 14.04 on a virtual machine, updated the a`apt-get` definitions and installed `curl`, `essetial-packages` and `ruby-build`. 

All these changes can be saved as an image, which allows you to quickly download it and add the read-write layer on top of it and start your container. Once you add the read-write layer on top of an image, this image becomes a container. 

Once your container is an a state that you would wish to preserve for duplication, commit your changes and the container is saved as an image.

### Useful Docker Commands

#### Building Image from Dockerfile

* running `sudo docker` will reveal a list of options that can be used. `build` is the option we're looking for in order to create an image from a Dockerfile.
* `sudo docker build -t ouruser/sinatra:v2`. We've specified our docker build command and used the `-t` flag to identify our new image as belonging to the user **ouruser**, the repository name **sinatra** and given it the tag **v2**. We've also specified the location of our Dockerfile using the `.` to indicate a Dockerfile in the current directory.
* https://docs.docker.com/articles/dockerfile_best-practices/

#### Container Linking

We will link a pythen web container to a postgres one:
* download the postgres db image, name it as **db** and create a container: `sudo docker run -d --name db training/postgres`
* download the python web app image, name it as **web**, assign the ports, link it to the **db** container and run it:`sudo docker run -d -P --name web --link db:db training/webapp python app.py`. This will link the new web container with the db container you created earlier. The --link flag takes the form `--link name:alias`, where `name` is the name of the container we're linking and `alias` is an alias for the link name.
* running `sudo docker inspect -f "{{.HostConfig.Links}}" web` should show you that the 2 containers are linked.

For some reason I was unable to run the `sudo docker inspect -f "{{.HostConfig.Links}}" web` command and get the expected result. However, when you run a docker web container and enter the console, you'll be able to see that the 2 containers are linked as expected:
* run docker container and enter console: `sudo docker run -t -i --rm --name web2 --link db:db training/webapp /bin/bash`
* once the container is loaded check for the links:
    * run `cat /etc/hosts`. 
    * run `apt-get install -yqq inetutils-ping && ping db`. Successful ping requests to the **db** container should be displayed. Exit the **ping** command by pressing `ctrl + c`
    * check the environment variables (`env`). You should see a series of db related variables, like `DB_NAME`, `DB_PORT_5432_TCP_ADDR`, `DB_PORT`, `DB_PORT_5432_TCP`, `DB_PORT_5432_TCP_PORT`, `DB_PORT_5432_TCP_PROTO`.

#### Data Containers

default is read-write, but 
read-only can be specified...

##### Adding a Data Volume Container

* create a volume data container: `sudo docker create -v /dbdata --name dbdata training/postgres` doesn't work, as there is no create anymore in the docker options. 
* create PostgreSQL container that use the above created data container: `sudo docker run -d --volumes-from dbdata --name db1 training/postgres`
* add another container: `sudo docker run -d --volumes-from dbdata --name db2 training/postgres`
* check the status of the containers created: `sudo docker ps`

#### Backup and Restore Data Volumes

In order to create backups, we'll launch a container that adds a `backups` folder and creates a backup of the `/dbdata` folder:

* `sudo docker run --volumes-from dbdata -v $(pwd):/backup ubuntu tar cvf /backup/backup.tar /dbdata`
* create a new container and run bash: `sudo docker run -v /dbdata --name dbdata2 ubuntu /bin/bash`
* untar the backup created earlier by running: `sudo docker run --volumes-from dbdata2 -v $(pwd):/backup busybox tar xvf /backup/backup.tar`

https://docs.docker.com/userguide/dockervolumes/
https://medium.com/@ramangupta/why-docker-data-containers-are-good-589b3c6c749e


