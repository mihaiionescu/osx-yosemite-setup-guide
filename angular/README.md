## Install Node and NPM

[Node.js](http://nodejs.org) is a platform built on [Chrome's JavaScript runtime](https://code.google.com/p/v8/) for easily building fast, scalable network applications. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient, perfect for data-intensive real-time applications that run across distributed devices.

[npm](https://www.npmjs.com) is most commonly used for managing Node.js modules. NPM is a package manager developed with nested dependencies handling in mind (http://maxogden.com/nested-dependencies.html).

* use Homebrew
* `brew install node`
* run `brew doctor` to check the installation and any dependencies.
* `node -v` and `npm -v` to check the installation

## Install Angular
* follow [official](https://docs.angularjs.org/tutorial/) documentation - throws back errors of not finding files:

    ```
    npm ERR! install Couldn't read dependencies
    npm ERR! Darwin 14.1.0
    npm ERR! argv "node" "/usr/local/bin/npm" "install"
    npm ERR! node v0.12.0
    npm ERR! npm  v2.5.1
    npm ERR! path /Users/mihai/Projects/package.json
    npm ERR! code ENOPACKAGEJSON
    npm ERR! errno -2
    
    npm ERR! package.json ENOENT, open '/Users/mihai/Projects/package.json'
    npm ERR! package.json This is most likely not a problem with npm itself.
    npm ERR! package.json npm can't find a package.json file in your current directory.
    
    npm ERR! Please include the following file with any support request:
    npm ERR!     /Users/mihai/Projects/npm-debug.log
    ```
* I get these errors because there was no `package-dependencies` file in the project folder. Installing Bower can be done separately (`sudo npm install -g bower`). 

* OR .. this one https://coderwall.com/p/cbacta/how-to-setup-your-mac-to-build-single-page-applications-with-angularjs-and-neo4j
* OR .. https://bardevblog.wordpress.com/2013/10/26/a-simple-tutorial-of-setting-up-and-using-bower-on-windows/

## Install Bower

[Bower](http://bower.io) is created solely for the front-end and is optimized with that in mind. The biggest difference is that npm does nested dependency tree (size heavy) while Bower requires a flat dependency tree (puts the burden of dependency resolution on the user).

Many projects use both is that they use `bower` for front-end packages and `npm` for developer tools like Yeoman, Grunt, Gulp, JSHint, CoffeeScript, etc.

Once `node` and `npm` are installed, `bower` can be installed through `npm`'s command line tool. We will install Bower globally, so the folder you're in when running the following command is not important:
```
sudo npm install -g bower
```

Follow the official [documentation](http://bower.io/#getting-started) to see how to install packages like `jquery`.

## Install Grunt

`sudo npm install -g grunt-cli`

Grunt is a powerful, feature rich task runner for Javascript. In brief, it lets you automate repetitive tasks like compiling coffeescript, minifying css, code validation etc. We’ll be using it to do all of that as well as prepare our code for development and deployment.

Grunt is going to whip through our project folder and prepare everything for us such as compiling our included Bootstrap SASS down to css.

## Install Yaoman

`sudo npm install -g yo`

Yeoman is used to generate the scaffolding of your app for you. It’ll create the basic folders, files and configurations to get you up and running quickly. Not only that but there are some great custom generators available to create apps of a particular kind – we’re going to use the nifty AngularJS generator.

One of the best features of Yeoman is the ability to use custom generators. We’re going to intall the AngularJS generator to help us get up and running with Angular as quick as possible.

## Problems

* running `npm install` throws access errors. This is a permissions issue in your home directory. To reclaim ownership of the .npm directory execute 
    ```
    sudo chown -R $(whoami) ~/.npm
    ```
* eegdfg

## References

http://www.sitepoint.com/kickstart-your-angularjs-development-with-yeoman-grunt-and-bower/




