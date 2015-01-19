# Vagrant

[Vagrant](https://www.vagrantup.com) is a very useful tool for creation lightweight, reproductible environments. Vagrant uses virtual boxes via an easy to use command line tool.

#### Installation

* Download the latest Vagrant for OSX from [here](https://www.vagrantup.com/downloads.html).
* Open the **.dmg** file and run the Vagrant.pkg file.
* Follow the on-screen instructions to finalise the installation.
* Check the installation by running `vagrant -v`.

#### Install Virtual Box

* Download the OSX latest Vistual Box release from the [list](https://www.virtualbox.org/wiki/Downloads).
* Open the **.dmg**, double click the **.pkg** file and follow the on-screen instructions.

## Test Vagrant and Virtual Box

Follow the Vagrant [start up guide](https://docs.vagrantup.com/v2/getting-started/project_setup.html).

## Install Vagrant Manager

Download the latest version from [here](http://vagrantmanager.com/downloads/).

## SublimeText Syntax Highlighting

In order to add syntax highlighting for Vagrantfile files, we'll edit the Ruby language default associations:
* Go to **Preferences > Browse Packages**.
* Open the Ruby language file: **Ruby/Ruby.tmLanguage**.
* Find the `<key>fileTypes</key>` associations.
* Add `<string>Vagrantfile</string>` in the `<array>` tag:

```
<key>fileTypes</key>
<array>
    <string>rb</array>
    <string>rbx</array>
    .....
    <string>Vagrantfile</array>
```

reference: https://medium.com/@iturgeon/vagrantfile-syntax-highlighting-in-sublime-text-92bb72a74361