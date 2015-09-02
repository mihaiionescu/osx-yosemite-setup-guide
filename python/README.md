## Install Python

The latest version of Python is Python 3.4.3. Since `python3` is so different from `python`, many still prefer to use the original Python.

#### Python

OSX Yosemite comes with Python pre-installed, but the version is not the latest one. In order to install the latest Python, you can use Homebrew:
```
brew install python
```
This will also install `setuptools` and `pip` as well. 

`setuptools` enables you to download and install any compliant Python software over a network (usually the Internet) with a single command (`easy_install`). It also enables you to add this network installation capability to your own Python software with very little work.

`pip` is a tool for easily installing and managing Python packages, that is recommended over easy_install. It is superior to easy_install in several ways, and is actively maintained.

```
$ which pip python
/usr/local/bin/pip
/usr/local/bin/python
```

#### Python3

The easiest way to install Python3 is to use Homebrew: `brew install python3`

This installs python3 and pip3 
```
$ which pip3 python3
/usr/local/bin/pip3
/usr/local/bin/python3
```