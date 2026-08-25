# 401_Read_03 - Express REST API

## [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

### Answers.1

1. Classes are a template for creating __.
    - Objects; defines properties and behaviors that objects created from said class should have.
2. Can a class declaration be hoisted?
    - no, not before it has been declared. Functions can. not classes.
    - JS moves calls to the top before code runs.
3. How would you describe a constructor and contextual “this” to a non-technical friend?
    - a blueprint for building new objects from a class; defines the criteria / parameters of what the new instance will fill in with, with actual data. think IDs (hair color, weight, height), think car features across manufacturers (model, color, transmission, seats, fuel), etc. `this` simply referes to the particular object worked on at the moment.

## [Using Express Routing](https://expressjs.com/en/guide/routing.html)

## Answers.2

1. Within Express, what does routing refer to?
    - determining how an Express app responds to a client's request for a particular endpoint (`/__`) and HTTP method (`GET`, `PUT`, `PATCH`, `DELETE`)
2. What is the difference between a route path and a route method?
    - Route path identifies the endpoint (`/`) resource the request applies to.
    - Route method refers to the action / HTTP operation bei.g done to/at the resource.
3. When is it appropriate to add `next` as a parameter to a route handler and what must you do if `next` has been passed to your middleware as a parameter?
    - `next` is added when the current handler isn't or shouldn't be the end of the request-processing chain; when middleware is not finished and another middleware or route handler should run after it;
      - `next()` must be called inside if used as parameter.

## [Express Routing](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)

### Answer.3

1. What is an Express Router?
    - a modular routing system that allows routes and middleware to be grouped and routed to, rather than putting every route inside the main server file. Easier to separate responsibilities per endpoint.
2. By what mean do we initialize `express.Router()` in an express server?
    - a router is created using `const router = express.Router();`, but we also need to import `const express = require('express');` before trying to use `router.get();`, `router.post();`, etc.
      - the router can be exported using `module.exports = router;`.
3. What do we use route middleware for?
    - performs an action on a request (CRUD) before it reaches the final route handler; frees up the amount of work the route handler has to do alone.

## Things I Want to Know More About

- more practice with `class`, `constructor`, `protoypes`.
- hoisting functions
- the use of `next`
