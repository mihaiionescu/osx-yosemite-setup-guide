# Sublime Text 3

Download [Sublime Text 3](http://www.sublimetext.com/3) open the **.dmg** file and move the app into the **Applications** folder.

Too keep the app in the Dock, **right click > Options > Keep in Dock**.

You can add a shortcut to the Terminal so that you can open files and folders in Sublime straight from the command line:
`$ ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl`

Once you do that, you can open folders using `subl .` or files `subl /path/to/file/my_file`.

In the next sections we will add Package Control and setup Sublime further.

## Preferences

One of the great advantages of Sublime Text is the ability to customise it easily. The following [gist](https://gist.github.com/mihaiionescu/7ec7c57950f9e0a2c9dc) contains the User Settings I currently use. 

#### Colour Scheme

After trying a large number of colour schemes, my weapon of choice is Base 16](). It provides a coherent colour scheme throughout the Terminal and text editors in your operating system. 
In order to add the Base 16 colour schemes to Sublime Text:
* Open a Terminal window
* **cd ~/Library/Application\ Support/Sublime\ Text\ 2/Packages**
* **git clone git://github.com/chriskempson/base16-textmate.git Base16**
* after the download is complete, you can choose a different colour theme from **Sublime Text > Preferences > Color Schemes > Base16**

#### Sidebar Theme




## Package Control

#### Install Package Control

Package Control is ...
In order to install Package Control, open Sublime's console (**ctrl + `**) and paste the following code:

```
import urllib.request,os,hashlib; h = '2deb499853c4371624f5a07e27c334aa' + 'bf8c4e67d14fb0525ba4f89698a6d7e1'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

Note: double check the installation command [here](https://packagecontrol.io/installation). Every release the command is changed. 

#### Useful Packages

-- TO BE ADDED --

## Sublime Linter

Inspiration: http://sourabhbajaj.com/mac-setup/SublimeText/SublimeLinter.html


-- TO BE ADDED --








