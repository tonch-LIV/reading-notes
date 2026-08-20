# 401_Read_02 - Intro to Node.js

## [Intro to NodeJS and Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction) 

### Answers.1  

1. Explain middleware, answer as though I were a non-technical recruiter.
2. Express the most popular ___.
    - [node web framework]
3. Express is “unopinionated.” What does that mean?
    - Express gives developers the freedom to decide *how* their application should be structured and *which* tools or libraries they want to use.
4. What is a module and why is modularity useful to us as developers?
    - a file referencing code that handles one task; can be re-used, easier to manage, and organize in the grand scheme of the project it is being used on.

## [What is NPM?](https://docs.npmjs.com/getting-started/what-is-npm)

### Answers.2

1. What version of npm are you running on your machine?
    - `11.6.1` on Git Bash; `10.8.2` on WSL Ubuntu
2. What command would you type to install a library/package called ‘jshint’ into your node project?
    - `npm install jshint`
    - `npm install --save -dev jshint`

## [What is TDD?](https://www.agilealliance.org/glossary/tdd/)

### Answers.3

1. Explain why tests are important. Please explain as though I were your non-technical elder.
    - Testing to make sure that regardless of what you did and the outcome; the changes you made did not affect something else.
    - When working on a car (oil change, spark splus, or whatever else); after you finish, turning the car over and maiking sure it still turns on, lights, blinkers and everything else still functions as expected.
2. What are three expected benefits of testing?
    - Fewer defects / bugs
    - less work down the line doing cleanup
    - better code legibility and design quality
3. Name at least 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.
    - forgetting to run test frequently
    - writing simople tests that don't verify any meaningful behavior
    - writing many test at once / large tests

- not maintaining or updating the test suite
- tests become so slow, they are no longer used (double whammy)
- not used by everyone on a team

## [CI/CD](https://www.youtube.com/watch?v=k2aNsQKwyOo)

### Answers.4

1. What are three benefits of Continuous Integration?
    - Problems are discovered earlier; code is tested during change integration.
    - Problems are smaller and easier to fix, rather than digging through huge blocks of code.
    - Improve software quality; tests verify application still works.
2. What is the difference between Continuous Delivery and Continuous Deployment?
    - Delivery - A person approves decision to deploy to production.
    - Deployment - Code is automatically deployed after passing test, no human approval.
3. Explain how GitHub fits into this process assuming the listener comes from a non-technical background
    - Github is the central location where teams store, chare, and manage code, tests can be implemented, and they can be triggered to run when changes are made.
      - A librarian / teacher are good examples; teachers check the contents of assignments to make sure you did the assignmnet and meet the criteria to receive a passing score; if not, then fail the check, fail the assignment. Librarians lend and receive books and expect them to be returned to a similar state it was lent out.

## Bookmark and Review

[nodeJS docs](https://nodejs.org/en/docs/)
[npm docs](https://docs.npmjs.com/)
[express docs](https://expressjs.com/en/4x/api.html)
[http status codes](https://www.restapitutorial.com/httpstatuscodes.html)
[supertest](https://github.com/visionmedia/supertest)
