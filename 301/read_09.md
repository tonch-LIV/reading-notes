# 301_Read_09 - Functional Programming

- [Functional Programming Concepts](#functional-programming-concepts)
  - [Pure Functions](#pure-functions)
    - [Benefits](#benefits)
  - [Immutability](#immutability)
  - [Referential Transparency](#referential-transparency)
  - [Answers.1](#answers1)
- [[Video] - Modules and require()](#video---modules-and-require---node-js-beginner-tutorial-6)
  - [`require()`](#require)
  - [Answers.2](#answers2)
- [Bookmark / Review](#bookmark--review)
- [Things To Learn More About](#things-to-learn-more-about)

This is important because...  
As projects become larger; the easier one makes it to manage and maintain, the easier it'll be to troubleshoot if something should occur.  
Small pure functions grouped into modules, can then be combined into larger projects.  

## [Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

Complex software gets in the way of functional programming. Functional programming must be easy to understand and modify, if called for. Concepts such as Pure Functions, Immutability, and Referential Transparency are the backbone to creating code (programs) that are easier to understand, test, and maintain in the long run.  

Functional Programming refers to a style of programming that aims to make code behave in a manner that it's expected based on how it's written to function; avoiding mutable data and changing state.  
Predictable inputs should produce predictable outputs.  

### Pure Functions

Functions should return the same output when given the same arguments, time after time; there should be no 'surprise' or odd data returns.  

Pure Functions should have no side effects; meaning it can not modify,  
Global Variables,  
External Objects,  
Files,  
Databases,  
User Interfaces,  
or anything beside it's own function.  

```js
/// an impure function changing the global variable

let counter = 1;

function increaseCounter() {
  counter++;
}
```

```js
/// a pure function where the original variable is taken in as an argument, processed inside the function, but never changing the global variable

function increaseCounter(counter) {
  return counter + 1;
}
```

#### Benefits

1. Easier Testing  
    - Instead of having complicated environments; testing becomes easier as we verify that the input leads to an expected output. No need for hidden dependencies.  
2. Predictability  
    - pure functions always behave consistently, therefore will always return the same result when given the same inputs; no need to concern or wonder about hidden state changes.  
3. Easier Maintenance  
    - Functions are isolated; meaning you can modify or alter one without worrying if another relies on it and might break its behavior.  

### Immutability  

Data that can not be changed after being created. Instead of modifications to an existing object; a new one is created.  
i.e. updating the contents of a variable vs creating a new variable with updated data and leaving the original unchanged.  

Functional programming favors immutability since data can not change unexpectedly, meaning debugging becomes simpler as bugs are easier to track and deal with, since code is more predictable.  

Immutable data structures also help support fault tolerance, concurrent programming, safer communication between process, to just name a few others, since data can not be changed or modified unexpectedly.  

### Referential Transparency  

When expressions or functions can be replaced by the actual value being returned.  
(*Note: Hard Coding?)  

Pure functions x Immutability = Referential Transparency  
Pure functions avoid side effects while,  
Immutability prevents unexpected changes,  
together, they make behavior predictable and transparent.  

### Answers.1

1. What is functional programming?
    - a programming style that emphasizes predictable, reusable, and maintainable code.  
2. What is a pure function and how do we know if something is a pure function?
    - Pure functions always return the same output for the same input,  
    - create no side effects.  
3. What are the benefits of a pure function?
    - easier testing,  
    - predictable behavior,  
    - better maintainability,  
    - easier debugging,  
    - less unintended interactions throughout the program.  
4. What is immutability?
    - data that can not(should not) be changed after being created. New data structures are created with updated values.  
5. What is Referential transparency?
    - when a resulting value can replace its producing expression without affecting the behavior of the program.  

## [[Video] - Modules and require() - Node JS Beginner Tutorial #6](https://www.youtube.com/watch?v=xHLd36QoS4k)

Modules are pieces of code found in one file, that can be re-used in other files. Modules help organize code and keep responsibilities separated.  
Very similar, (often?) interchangeable with Components.  

### `require()`

Used to load (import) a module and its functionality into another module where you'd like to use it.  

```js
const add = require('./add');
```

To make a module available, it must first be exported in its file of origin.  

```js
function add(a, b) {
  return a + b;
}

module.exports = add;
```

### Answers.2

1. What is a module?
    - a reusable, self-contained file containing code that can be imported into other files.  
    - Modules help organize and separate application functionality.  
2. What does the word 'require' do?
    - loads another module and returns whatever that module exports so it can be used in the current file.  
3. How do we bring another module into the file the we are working in?
    - the `require()` function.  
4. What do we have to do to make a module available?
    - export it using `module.exports = ...`.  

## Bookmark / Review

## Things To Learn More About

- Hidden dependencies / state.  
- Referential Transparency vs hard coding.  
- functional programming array methods (`.map()`, `.filter()`, `.reduce()`).  
- cases  of when to use `require()` vs `import`.  
