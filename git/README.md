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

```
git config --global push.default matching
```
These options will be added into the `~/.gitconfig` file. You can check the contents of this file using `vim ~/.gitconfig` command.

The [official Git setup](https://help.github.com/articles/set-up-git/) guide recommends the HTTPS method (over SSH). In order to set HTTPS connection, we will enable using Git password caching ([article](https://help.github.com/articles/caching-your-github-password-in-git/)):

* Check if **osxkeychain** is installed: `
git config --global credential.helper osxkeychain
`
* If the **osxkeychain** is **not** installed: 
    * Download it using curl: `curl -s -O \
https://github-media-downloads.s3.amazonaws.com/osx/git-credential-osxkeychain`.
    * Fix the permissions on the file so you can run it: `chmod u+x git-credential-osxkeychain`
    * Install the helper in the same directory as **git**: `sudo mv git-credential-osxkeychain \
"$(dirname $(which git))/git-credential-osxkeychain"`
* Tell git to use osxkeychain using the **credential.helper** config: `git config --global credential.helper osxkeychain`

The next time you clone an HTTPS URL that requires a password, you'll be prompted for your username and password, and to grant access to the OSX keychain. After you've done this, the username and password are stored in your keychain and you won't be required to type them in to Git again.

## DS_Store

Remember to always add `.DS_Store` (a hidden OSX system file added to all folders) to the `.gitignore` file for all git projects.

## Github app

Download the [Github app](https://mac.github.com) and open it. follow the on-screen instructions to set it up. This will create a SSH key in your Github account. This will be used by the app to communicate with your account.
A paid alternative is [Tower](http://www.git-tower.com).

Although a GUI git client has it's advantages, consider [using the command line](Link-to_git-command-line-tutorial-book-or-article) for the majority of your git-related tasks.

## Git Ignore File

The majority of your projects will ignore certain files. Use this [gitignore](git/git_ignore.md) example to add default ignore files.

## Git Repos Terminal Setup

Next we will set OSX Terminal to show the git branch and state.

https://gist.github.com/mihaiionescu/0545d1b52ab5be540bd1

-- TO BE ADDED --




