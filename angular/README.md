## Install Node
* use Homebrew
* brew install node
* brew doctor
* `node -v` and `npm -v` to check the installation

# Install Angular
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

* OR .. this one https://coderwall.com/p/cbacta/how-to-setup-your-mac-to-build-single-page-applications-with-angularjs-and-neo4j