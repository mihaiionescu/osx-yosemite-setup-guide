# Sublime Text 3

Download [Sublime Text 3](http://www.sublimetext.com/3) open the **.dmg** file and move the app into the **Applications** folder.

Too keep the app in the Dock, **right click > Options > Keep in Dock**.

You can add a shortcut to the Terminal so that you can open files and folders in Sublime straight from the command line:
`$ ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl`

Once you do that, you can open folders using `subl .` or files `subl /path/to/file/my_file`.

In the next sections we will add Package Control and setup Sublime further.

## Preferences

One of the great advantages of Sublime Text is the ability to customise it easily. The following [gist](https://gist.github.com/mihaiionescu/7ec7c57950f9e0a2c9dc) contains the User Settings I currently use. 

#### Sidebar Theme

I like my sidebar and general appeal of Sublime to be minimal and I am also a fan of the [Base16]() colour scheme. [Spacegray Theme](https://github.com/kkga/spacegray) combines a minimal theme with the Base16 colour scheme. Another advantage of this theme, it can be installed through the Package Control:
* Open Package Control **Tools > Command Palette (shift + cmd + p) >  Package Control: Install Package**
* Find **Spacegray - Theme** and hit Enter.
* Activate the Sidebar and Colour Theme:
    * Open User Preferences: **cmd + ,** or **Sublime Text > Preferences > Settings - User**
    * add the following options (*Note: the options are already part of the preferences in the above gist*)
    ```
    "theme": "Spacegray.sublime-theme",
    "color_scheme": "Packages/Theme - Spacegray/base16-ocean.dark.tmTheme"
    ```
* restart Sublime Text 3 in order for the theme to take effect.
* for different options see https://github.com/kkga/spacegray

## Package Control

#### Install Package Control

Package Control is ...
In order to install Package Control, open Sublime's console (**ctrl + `**) and paste the following code:

```
import urllib.request,os,hashlib; h = '2deb499853c4371624f5a07e27c334aa' + 'bf8c4e67d14fb0525ba4f89698a6d7e1'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

Note: double check the installation command [here](https://packagecontrol.io/installation). Every release the command is changed. 

#### Next we'll install some packages to improve Sublime Text for developing.


##### DashDoc

[DashDoc](https://github.com/farcaller/DashDoc#readme) helps you integrate [Dash](http://kapeli.com) into Sublime Text.

To install DashDoc, simply open Package Control (**cmd + shift + p**), type "package" and choose "Package Control: Install Package" option. In the search bar type "DashDoc" and just hit "Enter".





