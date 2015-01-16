# Bash (OSX Default Terminal)

## Bash Profile

#### Keyboard Shortcuts

By default, OSX Yosemite comes with some very useful keyboard shortcuts:
* go to the beginning of the line `crtl + a`
* go to the end of the line `ctrl + e`
* move one word at a time `alt + right/left arrow`

#### Auto Complete From History
**??????**


A very useful feature you can add to you Terminal is the ability to autocomplete the command from the command history. In order to do this, you must modify the **~/.bash_profile** file. 

* Open **Terminal** and run `subl ~/.bash_profile`
* Append the following key bindings:
```
# make bash autocomplete with up arrow/down arrow
bind '"\e[A":history-search-backward'
bind '"\e[B":history-search-forward'
```
* close and reopen the **Terminal**. Now you can start writing the command, then press the `up arrow` and you'll search through the commands you alrady used.

Reference: https://lcoppa.wordpress.com/2011/05/01/autocomplete-command-line-from-history-in-os-x-terminal/

#### Git Repository Color Theme

When working at a project that uses git for version control, it is very useful to know the current branch you're working on and weather or not you the latest changes are committed.
In order to display this information, we'll modify the `~/.bash_profile` file:

* Open **Terminal** app and run `subl ~/.bash_profile`
* Add the contents of this [gist](https://gist.github.com/mihaiionescu/bc4127187f85fc25fac4) at the end of the file.
* Restart the **Terminal** and navigate to a git repository folder.

## Colour Themes
    
####  Tomorrow

* Download the required files from [here](https://github.com/chriskempson/tomorrow-theme/tree/master/OS%20X%20Terminal). *Note: link might be outdated so please write to me and I will amend it.
* Open OSX Terminal **Preferences** (`cmd + ,`) **> Profiles > Settings > Import** and choose the .terminal file downloaded.
* Make **Tomorrow** the default theme
    * Choose the Tomorrow theme from the **Profile** list and click the **Default** button.
* Make Terminal window semi-transparent
    * Select Tomorrow theme from Profile list.
    * Choose **Window** tab.
    * From the **Background** section, click on **Colour & Effects**.
    * Set the **Opacity** option to 85%
    * Close the Preferences windows & restart the app.

#### Piperita

## Window Groups

Set specific Terminal tabs for every project.