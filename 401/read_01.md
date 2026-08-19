# 401_Read_01 - Intro to Node.js

- [Intro](#introduction-to-nodejs)
  - [Execution](#execution)
  - [Answers.1](#answers1)
- [Things to Learn More About](#things-to-learn-more-about)

## [Introduction to Node.js](https://www.sitepoint.com/an-introduction-to-node-js/)

Node.js is the environment which JavaScript, the programming language, can use to execute code outside of a browser environment.  

Browsers contain JS engines that they use to interpret and execute JS.  
Node will take an engine and give it additional capabilities to work beyond the environment (browser); such as files, networking, HTTP connections, and even OS functionality.  

Such as using `node server.js` (or other file) in the terminal.  

### Execution

Node is **event-driven** and **non-blocking**; this means that rather than waiting for one operation / task to complete, Node will continue handling other duties and return to completed task as they finish. Ideal for applications that handle multiple simultaneous requests.  

The use of `async` and `await`.  

Node is useful for;  
back-end / server-side JS,  
REST APIs / other API servers,  
apps with plenty of database and/or network operations,  
streaming data,  
CLI tools and automation scripts,  
JS development / building throigh the use of npm,  
and others.  

Even if a React application does not use Node as a production backend; it is still common for it to use Node during development for things like package mgmt, build tools, testing, linting, and other similar tasks.  

### Answers.1

1. How would you describe Node to a non-technical friend?  
    - Node.js allows JS to run outside of a browser. It lets developers use JS to build things like servers, APIs, command-line programs, and other applications that run directly on a computer.
      - similar to a kitchen; one cooks in a kitchen using a stove and/or oven, but Node is like having a outdoor kitchen / portable stove.
2. What does it mean that Node is a JavaScript runtime?  
    - The environment (engine) that can read **and** execute JS code.  
        - adds features that allow JS to interact with the system beyond the environment it is in.  
3. What is Node used for?  
    - Server-side development, building APIs, working w/ databases, running development tools (npm); very useful for applications that handle network and database requests and operations, due to being asynchronous and non-blocking.
4. Looking ahead at this module’s course schedule, What do you look forward to learning?
    - Learning more about back-end development concepts and how they are used. Strengthening my uderstanding of Node in general, but also, APIs, databases, app architecture, and how they all come together and work in projetcs.
5. What are your learning goals after reading and reviewing the class README?  
    - Strengthen JS understanding and backend development, become more comfortable and confident about building apps independently. Knowin *why* tools work, not just *how* to use them.

## Things to Learn More About

- other niche uses of Node.js  
- npm vs npx  
- different production backends, other than Node; alternatives...  
