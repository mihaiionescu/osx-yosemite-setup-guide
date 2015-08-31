# Install RVM and the Latest Ruby(2.2.0) and Rails

## RVM

[Ruby Version Manager](https://rvm.io), is one of the most popular tools that allow you to install and manage multiple versions of Ruby and Ruby on Rails on the same computer.

You can install RVM, Ruby and Rails using a single command, but because it also installs all the documentation, it is advisable to disable it in the beginning. Open **Terminal** and run:
`echo "gem: --no-document" >> ~/.gemrc`

Now you can proceed and install RVM and Ruby (check the [official documentation](https://rvm.io/rvm/install) for different options):

`curl -sSL https://get.rvm.io | bash -s stable --auto-dotfiles --autolibs=enable --rails`

This will take some time to finish. After the installation is complete, **quit and relaunch Terminal**, and then check the installation by running the `type rvm | head -1` command. If the response is `rvm is a function`, RVM was installed correctly.

Check the RVM, Ruby and Rails versions using:

`rvm -v` - you should get `rvm 1.26.9` or higher.

`ruby -v` - you should get `ruby 2.2.0p0` or higher.

`rails -v` - you should get `rails 4.2.0` or higher.

## Install Other versions of Ruby

* Make sure you have the latest stable version of RVM: `rvm get stable --autolibs=enable`
* Check the installed Ruby versions with RVM, use: `rvm list rubies`
* List all available Ruby versions, run: `rvm list known`
* Install ruby 2.1.5: `rvm install ruby-2.1.5`
* Make the 2.1.5 version the default version: `rvm use 2.1.5 --default`

## Useful gems

* [**bundler**](http://bundler.io/#getting-started) - provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed.
    * In order to install Bundler, simply run in Terminal `gem install bundler`.
    * After installing Bundler, simply specify your gems in the `Gemfile` file in your ruby / ruby on rails project and run `bundle install`.
* [**pg**](https://rubygems.org/gems/pg/versions/0.18.2) - the Ruby interface to the PostgreSQL RDBMS.
    * In order to install `pg`, #Postgres app needs to be installed first. Then, simply install by running in Terminal `gem install pg -- --with-pg-config=<path-to-pg_config>`. 


