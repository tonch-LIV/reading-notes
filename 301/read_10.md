# 301_Read_10 - In memory storage

- [Understanding the JavaScript Call Stack](#understanding-the-javascript-call-stack)
  - [Answers.1](#answers1)
- [JavaScript Error Messages + Debugging](#javascript-error-messages--debugging)
  - [Answers.2](#answers2)
- [Bookmark / Review](#bookmark--review)
- [Things to Learn More About](#things-to-learn-more-about)

This is important because...  
Its important to know the Call Stack is how functions are executed, Debugging is to investigate when a problem occurs during execution, and resouyrces to use (MDN) to learn what specific error messages mean.  

## [Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)

The JavaScript engine operates as a single-threaded interpreter through the use of its memory heap and a single call stack. This dictates the "hierarchy" within functions and their execution order.  

Being a single call stack means that functions are managed one at a time through a structure called **LIFO**; Last In, First Out; from 'top to bottom'. This is also referred to as Synchronous programming; tasks must be completed before moving on to the next task.  

Stack overflow is something that can occur when the stack has grown too large to effectively manage the execution of function invocations; could be caused by infinite recursions (repeatedly calling themselves).  

### Summary.1

The Call Stack tracks function execution.  
Function calls are pushed onto sack and go bottom-to-top, LIFO.  
As functions are executed, they are removed from the stack.  
Functions are executed one at a time.  
Inifnite recursionn causes stack overflow errors.  
Stack traces are useful when troubleshooting errors as they will show the sequence of calls that lead to the problem.  

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
    - to many function calls added to call stack, depleting memory (infinite recursion)

## [JavaScript Error Messages + Debugging](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

Error messages are important as they will include context as to how or what caused it to fail.  

**Reference Errors**  

Occurs when the JS engine cannot find something that is being referenced, invoked, or called.  

**Syntax Errors**  

Code structure is not understood by JS, therefore cannot execute the code. Either due to missing a comma, parenthesis, semi-colon, or the like.

**Range Errors**  

When a value falls outside the allowed range;  
i.e. invalid array length,  
invalid numeric values,  
invalid recursion depth.  

**Type Errors**  

When a value is used in a way its type does not support.

### Debugging  

**Stack Trace**  

A Stack Trace shows,
What failed,  
Where it failed,  
What function caused the fail / called it,  
The function that called that one.  

**Breakpoint**  
A breakpoint pauses the execution of a program at a specific line, so that code can be inspected.  

**Debugger**  
A keyword available for use when DevTools are open. Essentially, similar top a breakpoint.  

**`try... catch`**  

an `if... else` statement is for functions that account for the original desired output and what to do in case it cannot be met.

### Summary.2  

Debugging / troubleshooting revolves around;  
understanding error messages,  
reading stack traces,  
using breakpoints,  
inspecting code during its runtime.  

The most common JS errors are;  
Reference,  
Syntax,  
Range,  
Type.  

### Answers.2

1. What is a 'reference error'?
    - an attempt to access a variable or 'reference' that does not exist / has not been declared.
2. What is a 'syntax error'?
    - happens when code goes against JavaScript's rules of grammar and punctuation. Prevents execution even if everything else is defined and referenced correctly.
3. What is a 'range error'?
    - when a value falls outside the acceptable range for an operation.
4. What is a 'type error'?
    - the use of a value in a manner that does not accord with its data type.
5. What is a breakpoint?
    - a tool that pauses execution at specific points of execution of the program so a developer can inspect its current state.
6. What does the word 'debugger' do in your code?
    - it tells DevTools to pause execution at the point it is added to the program; a built-in breakpoint.

## Bookmark / Review

- [JavaScript errors reference on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)
  - Errors consist of name, message, and documentation explaining causesand solutions.  

## Things to Learn More About

- Synchronous and Asynchronous
