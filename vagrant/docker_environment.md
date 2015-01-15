# Running a Docker Based Environment With Vagrant

The end result will be a development environment which will only require `vagrant up` to setup a complete Docker-based environment. The components of this environment are:
* VM running Linux with Docker installed.
* Separate Docker containers for Rails, PostgreSQL and Redis.
* A shared folder linked to the Docker container so you can carry on editing Rails code on your development machine as you do now, and see those changes instantly reflected on `http://localhost:3000`.
* A simple interface for running all the normal Rails commands (`rake db:migrate`, `rails c` etc) in the Docker environment.

http://www.talkingquickly.co.uk/2014/06/rails-development-environment-with-vagrant-and-docker/