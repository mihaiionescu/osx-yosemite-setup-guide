# System Preferences

First thing you need to do, on any OS acutally, is update the system! For that: **Apple Icon > Software Update**. Also upgrade your OS in case you want to work on the latest OS. Yosemite is a free upgrade so please check that. At the moment of this writing, the latest version is 10.10.1.

## Users and Computer name

* Disable **Guest User > Allow guests to log in to this computer**
* **Login Options > Change** fast switching user menu to Icon
* Setup password, Apple ID, account image, etc.

## Trackpad

* Point and Click Tab
    * Enable **Tap to Click** 
    * Uncheck **Three Finger Drag**
* Scroll & Zoom Tab
    * Uncheck **Scroll direction: natural** - I am used to the "old" way of scrolling on Macs, but I got the "your scrolling the wrong way" plenty of times, so I'd say this one is optional
    * For any kind of photo/document editing, I consider useful having the **Smart Zoom** and **Rotate** options checked
* More Gestures Tab
    * I have **all** the options checked, but this again depends on your personal preference

## Display

I realised that I like the option of having more screen estate on the Retina Macbook by scaling it, so chose to run my display at 1920x1200. The other options for a scaled display are 1680x1050, 1280x800 and 1024x640, although I don't think there are too many people who would choose a smaller resolution than the original. 

You can change this setting from **System Preferences > Display > Scale > More Space** (1920x1200).

Instead of using a smaller screen resolution, consider using the Zoom function (**System Preferences > Accessibility > Zoom**). You can trigger using your trackpad by enabling the **Use scroll gesture with modifier keys to zoom** and choosing **Control** from the dropdown.

## Energy Saver

* Battery & Power Adapter Tabs
    * Increase the **Turn display off after** option to at least 5 mins

## Dock

* Change the **Size** to make the dock icons smaller
* Enable **Magnification** and set the magnified size slightly higher that the **Size**


I personally prefer the dock position at the bottom of the screen, but you can easily change that to either the left or right of the screen from **System Settings > Dock**.

## Finder

* Toolbar (**View > Customize Toolbar**)
    * Add **New Folder** and **Delete** options
* Preferences
    * General
        * Change **New Finder windows show** option to point to Home directory
    * Sidebar
        * Add **Home** and Code / Projects directories
        * Remove **All My Files**
        * Remove the **Shared** options - not really useful
    * Advanced
        * Enable **Show all filename and extensions**
        * Enable **Empty Trash securely**
* View Options
    * Show **Path Bar**, **Status Bar**
    * **View > As Columns**
    * Select Column View for all items in the sidebar
    * Enable **Show View Options (cmd + j) > Always open in column view** for all items in the sidebar
* Show hidden files:
    * `defaults write com.apple.finder AppleShowAllFiles -boolean true ; killall Finder`
* Create **.ec2** folder:
    * Open Finder window
    * Open **Go to**  (**cmd + shift + G**) and navigate to `~/`
    * Create a folder named **.ec2**

## Menubar

* Modify **Battery** preferences to **Show Percentage**

## Spotlight

* Uncheck **Fonts**, **Movies**, **Images**
* Uncheck **Finder search windows keyboard shortcut** option

## Safari

* Search
    * **Search engine > DuckDuckGo**
* General
    * Set **Safari opens with** option to **All windows from last session**
* Advanced
    * Enable **Show full website address**
    * Disable **Preload Top Hit in the background**
    * Enable **Show Develop menu in menu bar**
* Privacy
    * **Cookies and website data > Allow from websites I visit**
    * **Website use of location services > Prompt for each website once each day** 
* Install [Flash](http://get.adobe.com/flashplayer/). There are still a lot of websites that are using flash.

## Fonts

#### Input Font

[Input Font](http://input.fontbureau.com/) is a font created especially for development environments. What sets it apart from other coding fonts is the ability to personalise the code: you can choose either a Serif, Sans or Mono font type, the apparance of i and l (known as the most difficult letters for coding evironments).

You can download the customisation I use from [here](http://input.fontbureau.com/preview/?size=13&language=python&theme=solarized-dark&family=InputSans&width=300&weight=300&line-height=1.2&a=0&g=0&i=topserif&l=serifs_round&zero=0&asterisk=height&braces=straight&preset=sourcecode&customize=please).
In order to install it: 
* Open **Font Book**
* **Import** and navigate to the location you downloaded the font to.
* The font will be installed under the **User** section, to differentiate the system fonts from the ones you add.

#### Source Code Pro

[Source Code Pro](https://github.com/adobe-fonts/source-code-pro/releases/latest) is my choice of font for the Terminal. It is a monospaced font developed by Adobe, which designed it to work well in user interface (UI) environments.

* [download](https://github.com/adobe-fonts/source-code-pro/releases/latest) the latest version
* Open **Font Book** and **Import** the font.

## Accounts

* Add an **iCloud** account to sync Calendar, Contacts, Find My Mac, etc.
* Set Up Family
    * -- TO BE COMPLETED --
* iCloud Drive (**Only when all systems are on Yosemite and iOS 8**)
    * -- TO BE COMPLETED --

## Automatic Updates

-- TO BE COMPLETED --

## Troubleshooting










