# CakePHP Browser Detection Component : browser and OS version front-end detection 

 Browser Version And OS Version Detection Plugin

## Installation

* Clone/Copy the files in this directory into `app/Controller/Component/`
* Include the Browser Detection component in your controller:
   * `public $components = array('BrowserDetection');`

## Documentation

This Plugin offers a number of wrapper functions for these two great external libraries:

	 Chris Schuld's Browser Class 
	 (http://chrisschuld.com/) 
	 
	 Harald Hope's Full Featured PHP Browser/OS detection
	 (http://techpatterns.com/downloads/php_browser_detection.php


The method $browser->checkBrowserVersionPlatform() is a combination of the libraries' methods into one to give the ability to narrow down to a specific browser, browser version, os, and os version.
Will return true if the browser matches the given arguments. The browser version is a max check, so any version earlier than $maxVersionToCheck will also pass. If you just use
checkBrowserVersionPlatform(), it will default to check for Windows XP IE 7.0 or lower, true if it matches, false if not:

     $browser->checkBrowserVersionPlatform() //defaults are equal to:
     $browser->checkBrowserVersionPlatform(7, 'Internet Explorer', 'Windows', 'XP');  

details of passed checkBrowserVersionPlatform() vars are here, more detailed comments can be found in the Helper itself:

	 $maxVersionToCheck set a maximum version number (eg 7.0) 
	 $browserToCheck default is Internet Explorer
	 $platformToCheck  default is Windows
	 $OSVersion default is XP, set to null to not check version


Example useage without defaults, returns true if match, false otherwise:

	 $browser->checkBrowserVersionPlatform(9, 'Internet Explorer', 'Windows', 'Vista');  

Also comes with a handy Warning message element catered to users running Windows XP and IE 7.

lists of OS's and Browsers can be found in the library classes' comments.

## Versions

This plugin is compatible with CakePHP 1.3.x. and CakePHP 2.x.

