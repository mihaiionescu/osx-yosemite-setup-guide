# Homebrew

Homebrew allows you to easily install hundreds of open-source tools. The full instructions are available on the [Homebrew Wiki](https://github.com/Homebrew/homebrew/wiki/Installation), but you should only need to run the command that’s listed at the bottom of the [Homebrew site](http://brew.sh):

`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

Follow the on screen instruction. Remember that Terminal doesn't provide feedback when writing your password.

After the instalation is done, run `brew doctor` to check that there were no problems. If everything is ok, you should see:

```
$ brew doctor
Your system is ready to brew.
```

Unless otherwise specified in the output, you can move on to [installing **git**](/git/README.md)