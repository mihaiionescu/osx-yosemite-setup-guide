# Bash (OSX Default Terminal)

## Bash Profile

#### Keyboard Shortcuts

#### Auto Complete From History

A very useful feature you can add to you Terminal is the ability to autocomplete the command from the command history. In order to do this, you must modify the **~/.bash_profile** file. 

* Open **Terminal** and run `subl ~/.bash_profile`
* Append the following key bindings:
```
# make bash autocomplete with up arrow/down arrow
bind '"\e[A":history-search-backward'
bind '"\e[B":history-search-forward'
```
* close and reopen the **Terminal**.

Reference: https://lcoppa.wordpress.com/2011/05/01/autocomplete-command-line-from-history-in-os-x-terminal/

#### Git Repository Color Theme

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