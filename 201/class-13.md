# STORAGE AND YOU

## the current state of things

Cookies are terrible because a lot of them transmit redundant data potentially slowing down your browsing. They really are only big enough to impact your performance but not large enough to hold anything meaningful.

There used to be userData which was an XML-Based structure, trusted domains could store up to 640kb. 

in 2002 along comes FLASH (no longer supported, you old hat now). It had flash cookies which were locally stored data that could hold 100kb per domain. Eventually it was modded to accept increments in a factor of 10, 100kb ->1Mb -> 10Mb -> 100Mb etc...

Now we have HTML 5 storage. Which allows pages to store key/value pairs. 

You store data based on a named key and then you can retreive that data with teh same key. The named key is a string and the data can be any type. 

the storage event is supported everywhere the localstorage object is supported. Which includes IE8 (gross). 

You can even add event listeners and callback to it, and attach events. 

The limitations of standard HTML 5 storage is 5Mb this is how much storage space each origin gets by default. At the time of writing this, no browser supports the ability to add more storage.

One of the great things is taht with HTML5 storage you can save board state in siomple games. So when you leave and return, the game is exactly where you left off in the browser. This has allowed for many more browser games to develop.

You can even use the storage space to affect things such as if there is a key/value detected, you can call fora resume game/continue rather than just a start nrew game. Alternitively that option can be greyed out if there is no key/value.

the present condition of storage is pretty solid right now and a new API has been standardized and implemented across browsers. 

One vision that competes is called SQL, the web SQL Database ahs only been implemented by 4 browsers at the time of this writing. Safari, chrome 4.0+, opear 10.5+ Iphone 3.0+ and android 2.0+. 

SQL though is a braod term as there are so many different types of SQL used by their own companies, like microsof, and adobe use their own versions. So in order to pin down what you're talking about you need to say SQL that shipped with blahblahblah. 