# 201_Read_13

- [Website Local Storage](#website-local-storage)
  - [Om nom nom! Cookies](#om-nom-nom-cookies)
  - [Local Storage on HTML5 Browsers](#local-storage-on-html5-browsers)
  - [Amswers](#answers)
- [Past, Present, and Future of Web App Local Storage](#past-present-and-future-of-web-app-local-storage)
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

## Past, Present, and Future of Web App Local Storage

## Things I Want To Know More About
