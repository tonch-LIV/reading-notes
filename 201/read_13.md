# 201_Read_13

- [Website Local Storage](#website-local-storage)
  - [Om nom nom! Cookies](#om-nom-nom-cookies)
  - [Local Storage on HTML5 Browsers](#local-storage-on-html5-browsers)
  - [Answers](#answers)
- [Past, Present, and Future of Web App Local Storage](#past-present-and-future-of-web-app-local-storage)
  - [HTML5 Storage](#html5-storage)
- [Things I Want To Know More About](#things-i-want-to-know-more-about)

This is important because...  
knowing useful scenarios where local storage could benefit the user experience, but also knowing where it does not need to be included.

## [Website Local Storage](https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/)

**HTTP** by default is *stateless*, meaning that say you were to close a web app, then load it back up; nothing would be "saved" / its state is reset.  

This can be remedied by "storing the state"; usually server-side, and through the use of a **user account**.  
The method of using a *user account* to save the state, can itself be circumvented through the use of **local storage**.  

Local storage is useful for;

- Caching data from sites that take longer to load.
- Keeps you from being banned from services, with help from caches.
- Store state of interfaces.

### Om nom nom! Cookies

Classic cookies and the crumbs they leave behind...  

**Cookies** have been, for a long time been used as a method of local storage.  
Cookies are locally saved text files that are connected to the respective domain of the page the file contents are saved from. They do have their limitations and connotations tied with their use.

### Local Storage on HTML5 Browsers

On modern HTML5 browsers, using local storage is as easy as defining the `localStorage` object, the `setItem()`, `getItem()` methods. Example below;

```js
localStorage.setItem('favoritesport','skiing');

var sport = localStorage.getItem('favoritesport');
// -> "skiing"
```

Removing an item can be done through the `removeItem()` method;

```js
localStorage.removeItem('favoritesport');
var taste = localStorage.getItem('favoritesport');
// -> null
```

### Answers

1. Why would a developer use local storage for a web application?
    - when pages are known to take a while to load; "store the state" as the user last left it; lessen the load on the network bandwidth / request & delivery of content.
2. What information should not be stored in local storage?
    - personal identity information;
3. Local storage can store what type of data? How would you convert it to that type before storing?
    - stored as strings; must be converted through the use of `JSON.stringify()` and `JSON.parse()`.

## [Past, Present, and Future of Web App Local Storage](https://clementbuchanan.github.io/reading-notes/code201Class13.html)

(**\* Broken Link, had to search for elsewhere...**)

Local storage triumphs due to being able to store information in the registry, INI files, XML files, embedded databases, and in the OS's own file format invention.  

Whereas web apps can only store data in mainly cookies which are prone to slowing down the web app by constantly transmitting data, due to being included with HTTP requests. If requests are sent through standard HTTP rather than HTTPS (TLS/SSL), the data being sent is being sent unencrypted. Cookies are also limited in size (4KB).  

Before HTML5, Flash objects were seen as an improvement over cookies functionality in both speed and data size, granting 100KB of storage per domain.  

### HTML5 Storage

Data stored in `key/value` pairs, which when the site/page is closed and or otherwise navigate away from it; will remain. Referred to as **Local Storage** or **DOM Storage** and seen as a much more secure alternative.  

## Things I Want To Know More About

- `JSON.stringify()` and `JSON.parse()` methods.
- Flash objects / plug-ins
- Google Gears / web SQL / SQLite
