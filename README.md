# js-popunder

**Project development discontinued!**

2013-11-18: I've grown tired of playing a mouse-and-cat game with Google in order to make the pop-under work. Hence, I regret to announce that after over a year of maintaining this project, I've decided to abandon it.

Thanks for anyone who contributed to this repo with either code or advice. Feel free to take this code, fork it, work it and make it work for you.

Cheers!

-----

**js-popunder** is a pure javascript function for creating pop-under windows

Usage
-----
Popunders are popup windows that open behind the currently active browser window.
The latest version of this script opens popunders on document.onclick.

Options
-------
- "sUrl": The url to open
- "sConfig": paramaters object (optional)

Available Parameters
-------
- "name": The name of the popunder window (defaults to a random number)
- "width": The width of the popunder (defaults to opener's width)
- "height": The height of the popunder (defaults to opener's height)
- "top": Popunder position from top (defaults to 0)
- "left": Popunder position from left (defaults to 0)
- "wait": Interval/wait time between popunders (in seconds, defaults to 3600 = 1 hour)
- "cap": Max daily popunders per domain (capping, defaults to 2)
- "cookie": Cookie name to be used (defaults to "__.popunder")

Compatibility
-------
- Google Chrome 10-30
- Mozilla Firefox 3-23
- Microsoft Internet Explorer 6-11
- Apple Safari 6

Known Issues
-------
- Pop-under windows does not work in Chrome 31+ (opens as pop-ups)

Examples
-------
This example opens google.com in full screen using default settings:

	jsPopunder('http://www.google.com');


This example opens google.com in a 500x500 window

	jsPopunder('http://www.google.com', {
		name: 'googleWindow', 
		width: 500, 
		height: 500
	});

Full example:

	jsPopunder('http://www.google.com', {
		name: 'googleWindow', 
		width: 1025, 
		height: 640, 
		top: 0, 
		left: 0, 
		wait: 1800, 
		cap: 10, 
		cookie: 'googPop'
	});

Enjoy!