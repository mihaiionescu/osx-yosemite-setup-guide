# Homebrew

Homebrew allows you to easily install hundreds of open-source tools. The full instructions are available on the [Homebrew Wiki](https://github.com/Homebrew/homebrew/wiki/Installation), but you should only need to run the command that’s listed at the bottom of the [Homebrew site](http://brew.sh):

`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Follow the on screen instruction. Remember that Terminal doesn't provide feedback when writing your password.

After the instalation is done, run `brew doctor` to check that there were no problems. If everything is ok, you should see:

```
$ brew doctor
Your system is ready to brew.
```

Unless otherwise specified in the output, you can move on to [installing git](git/README.md).

#### Common Homebrew Warnings

##### PATH Inconsistency

If you get `Warning: /usr/bin occurs before /usr/local/bin` when running `brew doctor`, run the command below, as recommended by Homebrew:

`$ echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile`

Quit & relauch Terminal, then run `brew doctor` again. You should be ready to brew.

##### Cellar folder doesn't exists

If you get `Error: No such file or directory - /usr/local/Cellar` when running `brew doctor`, create the Cellar folder:

`$ sudo mkdir /usr/local/Cellar`

Quit & relauch Terminal, then run `brew doctor` again. You should be ready to brew.

For other common problems with Homebrew, check http://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/#step-3




