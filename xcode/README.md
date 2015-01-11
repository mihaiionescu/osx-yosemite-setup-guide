# XCode

Install [XCode](https://developer.apple.com/xcode/) from the App store or the Apple developer website.

For installing XCode command line tools run the command

```
xcode-select --install
```
It'll prompt you to install the command line tools. Follow the instructions and now you have XCode and XCode command line tools both installed and running.

#### Accept Command Line Tools Terms & Conditions

Open **Terminal** app (you can find it in **Applications > Utilities** folder) and run `sudo gcc --version`. This will prompt you to agree to Apple's XCode Terms and Conditions. Follow the on screen instructions.

If you run `gcc --version` again, and the installation was successful, you should see something similar to:
```
$ gcc--version
Configured with: --prefix=/Applications/Xcode.app/Contents/Developer/usr --with-gxx-include-dir=/usr/include/c++/4.2.1
Apple LLVM version 6.0 (clang-600.0.56) (based on LLVM 3.5svn)
Target: x86_64-apple-darwin14.0.0
Thread model: posix
```