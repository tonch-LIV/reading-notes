# 301_Read_07

- [Intro to Node.js](#introduction-to-nodejs)
- [Reasons to Pair Program](#6-reasons-for-pair-programming)
- [Bookmarks to Review](#bookmark-and-review)
- [Things I want to Know More About](#things-i-want-to-know-more-about)

This is important because...  
knowing how things opeate in the back half of a deployed live web service can lead one to better results, by creating a more polished product.  

## [Introduction to Node.js](https://www.sitepoint.com/an-introduction-to-node-js)

A JavaScript runtime environment (built on Chrome
s V8 engine) that allows for the execution of JavaScript on the server(remote), rather than the browser(locally). The V8 engines runs in Chrome and other chromium-based web browsers and is responsible for compiling javascript directly to native machine code, all with optimal performance in mind.  

Node is a standalone program, equipped with various enhanced features (file system API, HTTP library, and other OS related utility methods) and does not run in the browser.  

 There is benefit from using and interchanging between different [versions](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/). npm (node package manager) manages and handles installation of packages necessary for javascript development.  
Modern javascript (ES6) is very well supported by node, allowing you to use modern syntax and avoid compatability issues.  

`package.json` lists dependencies (among other contents) used within a project / directory from the libraries found on `node_modules`.  
`node_modules` should not be added to version control, but `package.json` should, as it'll allow other developers who'd like to clone your project down, to know what dependencies are needed to run.

Example of what can be installed with node/npm are build tools that'll bundle JS files and assets as static assets, run test, lint code, check styling, and many more.

More on the relationship between Node and modern JavaScript and their [anatomy](https://www.sitepoint.com/anatomy-of-a-modern-javascript-application/).

### Answers.1

1. What is node.js?
    - a runtime environment that allows javascript to run outside a web browser. Used in the back-end for servers.
2. In your own words, what is Chrome's V8 JavaScript Engine?
    - handles reading and executing javascript; translates javascript to machine code.
3. What does it mean that node is a JavaScript runtime?
    - provides what is needed to run / execute outside a browser; allowed to interact with the OS.
4. What is npm?
    - node package manager;
      - allows devs to install libraries/packages.
      - share code.
      - use toolds created by other devs
5. What version of node are you running on your machine?
    - v24.11.0 on Windows & Git Bash
    - v20.20.2 on WSL Ubuntu
6. What version of npm are you running on your machine?
    - 11.6.1 on Git Bash
    - 10.8.2 on WSL Ubuntu
7. What command would you type to install a library/package called 'jshint'?
    - npm install jshint
8. What is node used for?
    - back-end web srevers
    - REST APIs
    - CLI tools
    - automation

## [6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

1. What are the 6 reasons for pair programming?
    - Greater efficiency
    - Collaboration
    - Learning from peers
    - Social skills
    - Job interview preparation
    - Work environemnt preparation
2. In your experience, which of these reasons have you found most beneficial?
    - Learning from peers
3. How does pair programming work?
    - driver and navigator

## Bookmark and Review

- [Geocoding API Docs](https://locationiq.com/)
- [Axios docs](https://www.npmjs.com/package/axios)
- [MDN async and await](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await)

## Things I Want to Know More About

- more on npm and its companions (Ruby, PHP, etc.)
