# Installing Git and Github Setup

[Git](http://git-scm.com) is a [version control system](http://en.wikipedia.org/wiki/Revision_control) very popular amongst developers. After installing Homebrew, installing git is a very simple task:

```
brew update
brew install git
```

After the installation is complete, run `brew doctor`. Check [Homebrew warnings](homebrew/README.md) section if homebrew displays any warnings / errors.

In order to check git installation, run `git --version`.
Running `which git` should output `/usr/local/bin/git`.

Next we will set your [Github](https://github.com) user and email for git.

If you do have a Github account, create one. Add your user name and email in git using:
```
$ git config --global user.name "Your Github Full Name"
$ git config --global user.email "Your Github Email Address"
```
These options will be added into the `~/.gitconfig` file. You can check the contents of this file using `vim ~/.gitconfig` command.

The [official Git setup](https://help.github.com/articles/set-up-git/) guide recommends the HTTPS method (over SSH). In order to set HTTPS connection, we will enable using Git password caching ([article](https://help.github.com/articles/caching-your-github-password-in-git/)):



```
$ git config --global credential.helper osxkeychain
```