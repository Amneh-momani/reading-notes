# THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS

## DIVING IN
ersistent local storage is one of the areas where native client applications have held an advantage over web applications. For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state.
##  They are three potentially dealbreaking downsides:
+ Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
+ Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)
+ Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful

## What we really want is

+ a lot of storage space
+ on the client
+ that persists beyond a page refresh
+ and isn’t transmitted to the server

## A BRIEF HISTORY OF LOCAL STORAGE HACKS BEFORE HTML5
In 2002, Adobe introduced a feature in Flash 6 that gained the unfortunate and misleading name of “Flash cookies.” Within the Flash environment, the feature is properly known as **Local Shared Objects**.


 Briefly, it allows Flash objects to store up to 100 KB of data per domain. Brad Neuberg developed an early prototype of a Flash-to-JavaScript bridge called **AMASS** (AJAX Massive Storage System), but it was limited by some of Flash’s design quirks.
 
 
  By 2006, with the advent of **ExternalInterface** in Flash 8, accessing LSOs from JavaScript became an order of magnitude easier and faster. Brad rewrote AMASS and integrated it into the **popular Dojo** Toolkit under the moniker **dojox.storage** . Flash gives each domain 100 KB of storage “for free.” Beyond that, it prompts the user for each order of magnitude increase in data storage (1 Mb, 10 Mb, and so on).

In the meantime, Brad Neuberg and others continued to hack away on dojox.storage to provide a unified interface to all these different plugins and APIs. By 2009, dojox.storage could auto-detect (and provide a unified interface on top of) Adobe Flash, Gears, Adobe AIR, and an early prototype of HTML5 storage that was only implemented in older versions of Firefox.



As you survey these solutions, a pattern emerges: all of them are either specific to a single browser, or reliant on a third-party plugin. Despite heroic efforts to paper over the differences (in dojox.storage), they all expose radically different interfaces, have different storage limitations, and present different user experiences. 

So this is the problem that HTML5 set out to solve: to provide a standardized API, implemented natively and consistently in multiple browsers, without having to rely on third-party plugins.


## INTRODUCING HTML5 STORAGE
What I will refer to as “HTML5 Storage” is a specification named **Web Storage** , which was at one time part of the HTML5 specification proper, but was split out into its own specification for uninteresting political reasons. Certain browser vendors also refer to it as “Local Storage” or “DOM Storage.” The naming situation is made even more complicated by some related, similarly-named .

>function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }  
}

## USING HTML5 STORAGE

_HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key._

 The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. 
 
 However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.

>interface Storage {
  getter any getItem(in DOMString key);
  setter creator void setItem(in DOMString key, in any data);
};

_Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception._

## TRACKING CHANGES TO THE HTML5 STORAGE AREA

If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something. For example, if you set an item to its existing value or call clear() when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.

>if (window.addEventListener) {
  window.addEventListener("storage", handle_storage, false);
} else {
  window.attachEvent("onstorage", handle_storage);
};

## LIMITATIONS IN CURRENT BROWSERS

In talking about the history of local storage hacks using third-party plugins, I made a point of mentioning the limitations of each technique, such as storage limits. I just realized that I haven’t mentioned anything about the limitations of the now-standardized HTML5 Storage. I’ll give you the answers first, then explain them. The answers, in order of importance, are “5 megabytes,” “QUOTA_EXCEEDED_ERR,” and “no.”

“5 megabytes” is how much storage space each origin gets by default. This is surprisingly consistent across browsers, although it is phrased as no more than a suggestion in the HTML5 Storage specification. One thing to keep in mind is that you’re storing strings, not data in its original format. If you’re storing a lot of integers or floats, the difference in representation can really add up. Each digit in that float is being stored as a character, not in the usual representation of a floating point number.


## HTML5 STORAGE IN ACTION
How does it work? Every time a change occurs within the game, we call this function:

>function saveGameState() {
    if (!supportsLocalStorage()) { return false; }
    localStorage["halma.game.in.progress"] = gGameInProgress;
    for (var i = 0; i < kNumPieces; i++) {
	localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
	localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
    }
    localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
    localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
    localStorage["halma.movecount"] = gMoveCount;
    return true;
}

The most important part of this function is the caveat that I mentioned earlier in this chapter, which I’ll repeat here: Data is stored as strings. If you are storing something other than a string, you’ll need to coerce it yourself when you retrieve it. For example, the flag for whether there is a game in progress (gGameInProgress) is a Boolean. In the saveGameState() function, we just stored it and didn’t worry about the datatype:

**localStorage["halma.game.in.progress"] = gGameInProgress;**

Similarly, the number of moves is stored in gMoveCount as an integer. In the saveGameState() function, we just stored it:

**localStorage["halma.movecount"] = gMoveCount;**

But in the resumeGame() function, we need to coerce the value to an integer, using the parseInt() function built into JavaScript:

**gMoveCount = parseInt(localStorage["halma.movecount"]);**


## BEYOND NAMED KEY-VALUE PAIRS: COMPETING VISIONS
While the past is littered with hacks and workarounds, the present condition of HTML5 Storage is surprisingly rosy. A new API has been standardized and implemented across all major browsers, platforms, and devices. As a web developer, that’s just not something you see every day, is it? But there is more to life than “5 megabytes of named key/value pairs,” and the future of persistent local storage is… how shall I put it… well, there are competing visions.


Of course, if you’ve used more than one database product in your life, you are aware that “SQL” is more of a marketing term than a hard-and-fast standard. (Some would say the same of “HTML5,” but never mind that.) Sure, there is an actual SQL specification (it’s called SQL-92), but there is no database server in the world that conforms to that and only that specification. There’s Oracle’s SQL, Microsoft’s SQL, MySQL’s SQL, PostgreSQL’s SQL, and SQLite’s SQL. Indeed, each of these products adds new SQL features over time, so even saying “SQLite’s SQL” is not sufficient to pin down exactly what you’re talking about. You need to say “the version of SQL that shipped with SQLite version X.Y.Z.”

If you’ve done any SQL database programming, these terms probably sound familiar. The primary difference is that the object store has no structured query language. You don’t construct a statement like "SELECT * from USERS where ACTIVE = 'Y'". Instead, you use methods provided by the object store to open a cursor on the database named “USERS,” enumerate through the records, filter out records for inactive users, and use accessor methods to get the values of each field in the remaining records. An early walk-through of IndexedDB is a good tutorial of how IndexedDB works, giving side-by-side comparisons of IndexedDB and Web SQL Database.

