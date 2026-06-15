# 301_Read_10 - In memory storage

- [Understanding the JavaScript Call Stack](#understanding-the-javascript-call-stack)
  - [Answers.1](#answers1)
- [JavaScript Error Messages + Debugging](#javascript-error-messages--debugging)
  - [Answers.2](#answers2)
- [Bookmark / Review](#bookmark--review)
- [Things to Learn More About](#things-to-learn-more-about)

This is important because...  

## [Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)

The JavaScript engine operates as a single-threaded interpreter through the use of its memory heap and a single call stack. This dictates the "hierarchy" within functions and their execution order.  

Being a single call stack means that functions are managed one at a time through a structure called **LIFO**; Last In, First Out; from 'top to bottom'. This is also referred to as Synchronous programming; tasks must be completed before moving on to the next task.  

Stack overflow is something that can occur when the stack has grown too large to effectively manage the execution of function invocations; could be caused by infinite loops.  

### Answers.1

1. What is a 'call'?
    - a function being invoked / executed; `functionName();`
2. How many 'calls' can happen at once?
    - one, single-threaded call stack; many can be loaded on the stack waiting.
3. What does LIFO mean?
    - Last In, First Out.
4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
    - declarations of functions one, two, three;
      - invocation of one;
        - function one invokes two;
          - two invokes three;
            - three console.logs "Done".
5. What causes a Stack Overflow?
    - to many function calls added to call stack, depleting memory (infinite loops)

## [JavaScript Error Messages + Debugging](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

### Answers.2

1. What is a 'reference error'?
2. What is a 'syntax error'?
3. What is a 'range error'?
4. What is a 'type error'?
5. What is a breakpoint?
6. What does the word 'debugger' do in your code?

## Bookmark / Review

- [JavaScript errors reference on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)

## Things to Learn More About

- Synchronous and Asynchronous
