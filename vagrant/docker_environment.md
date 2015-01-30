# Running a Docker Based Environment With Vagrant

The end result will be a development environment which will only require `vagrant up` to setup a complete Docker-based environment. The components of this environment are:
* VM running Linux with Docker installed.
* Separate Docker containers for Rails, PostgreSQL and Redis.
* A shared folder linked to the Docker container so you can carry on editing Rails code on your development machine as you do now, and see those changes instantly reflected on `http://localhost:3000`.
* A simple interface for running all the normal Rails commands (`rake db:migrate`, `rails c` etc) in the Docker environment.

http://www.talkingquickly.co.uk/2014/06/rails-development-environment-with-vagrant-and-docker/

## Docker

### Generalities

#### Container vs Image

Images are containers in a certain state. Say you installed ubuntu 14.04 on a virtual machine, updated the a`apt-get` definitions and installed `curl`, `essetial-packages` and `ruby-build`. 

All these changes can be saved as an image, which allows you to quickly download it and add the read-write layer on top of it and start your container. Once you add the read-write layer on top of an image, this image becomes a container. 

Once your container is an a state that you would wish to preserve for duplication, commit your changes and the container is saved as an image.

### Useful Docker Commands

#### Container Linking

We will link a pythen web container to a postgres one:
* download the postgres db image, name it as **db** and create a container: `sudo docker run -d --name db training/postgres`
* download the python web app image, name it as **web**, assign the ports, link it to the **db** container and run it:`sudo docker run -d -P --name web --link db:db training/webapp python app.py`. This will link the new web container with the db container you created earlier. The --link flag takes the form `--link name:alias`, where `name` is the name of the container we're linking and `alias` is an alias for the link name.
* running `sudo docker inspect -f "{{ .HostConfig.Links }}" web` should show you that the 2 containers are linked.

For some reason I was unable to run the `sudo docker inspect -f "{{ .HostConfig.Links }}" web` command and get the expected result. However, when you run a docker web container and enter the console, you'll be able to see that the 2 containers are linked as expected:
* run docker container and enter console: `sudo docker run -t -i --rm --name web2 --link db:db training/webapp /bin/bash`
* once the container is loaded check for the links:
    * run `cat /etc/hosts`. 
    * run `apt-get install -yqq inetutils-ping && ping db`. Successful ping requests to the **db** container should be displayed. Exit the **ping** command by pressing `ctrl + c`
    * check the environment variables (`env`). You should see a series of db related variables, like `DB_NAME`, `DB_PORT_5432_TCP_ADDR`, `DB_PORT`, `DB_PORT_5432_TCP`, `DB_PORT_5432_TCP_PORT`, `DB_PORT_5432_TCP_PROTO`.

#### Data Containers

##### Adding a Data Container




