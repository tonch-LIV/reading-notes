# 201_Read_10

- [Where Did We Go Wrong](#where-did-we-go-wrong-w-javascript)
  - [Syntax](#syntax-errors)
  - [Logic](#logic-errors)
  - [Common Errors](#common-errors)
  - [Answers.1](#answers1)
- [Bugs in my Java(Script)](#debugging-javascript)
  - [JavaScript Console](#javascript-console)
  - [Answers.2](#answers2)
- [HTML Bugs](#html-bugs)
- [CSS Buggin](#css-buggin)

This topic matters because...  
it is important to know how to fix something, but more importantly, how to begin investigating what went wrong and what tools to use that might help troubleshoot.  

## [Where Did We Go Wrong (w/ JavaScript)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/What_went_wrong)

### Syntax Errors

Mainly spelling, punctuation, or other minor errors easily rectified. Can cause program to stop halfway through or to not run at all. Error messages usually help pinpoint exact spot where error(s) are found.

A web browser console is great at providing error messages regarding syntax; gives you info on line error happened on and somewhat detailed message about what caused the program to break.

### Logic Errors

Code simply does not make sense / compute correctly, and ergo does not produce intended / desired result. May be harder to fix from lack or error messages.

To track this down, a good place to start would be where the code is not operating as expected and where either backwards nor forwards from there. The `console.log` function is also a great tool to selectively run code and see what the output is.

### Common Errors

Wrong use of assignment and/or comparison operators.  
Missing parenthesis, semicolon, colon, curly braces, quotes or other punctuation.  

### Answers.1

1. Name some key differences between a Syntax Error and a Logic Error.
    - Syntax is mistake in structure of code that breaks js rules; is detected immediately when runnin and will stop execution (types, punctuation).
    - Logic is when code runs, but does not do desired operation.
2. List a few types of errors that you have encountered in past lab assignments and explain how you were able to correct them.
    - I've encountered both logic and syntax; stylesheet linking, keywords mispelling and these are easily remedied after viewing the console. logic are a bit more difficult and on these Ive had to rely on a compiler / chatgpt.
3. How will this topic continue to influence your long term goals?
    - by being more methodical and systematic in my troubleshooting

## [Debugging JavaScript](https://developer.mozilla.org/en-US/docs/Learn_web_development/Howto/Tools_and_setup/What_are_browser_developer_tools#the_javascript_debugger)

Used to identify problems that would prevent code from executing by setting breakpoints and through watching the value of variables as they run.  

- **Watch expressions**: show added variables.
- **Breakpoints**: pause execution expressions.
- **Call stack**: shows code that was executed to get to current line.
- **Scopes**: Shows visible values throughout code structure.

### JavaScript Console

Provides immediate response by allowing the execution of chosen lines of code at will from file currently loaded in browser. Also helpful in reporting errors encountered as browser tries to load and run the file.

### Answers.2

1. How would you describe the JavaScript Debugger tool and how it works to someone just starting out in software development?
    - allows us to pause the code while its running to inspect whats its happening step-by-step.
2. Define what a breakpoint is.
    - a marker placed on code to stop it fom running any further
      - Identify logic errors, understand flow, inspect variables.
3. What is the call stack?
    - how js keeps track of function calls; last in -> first out

## HTML Bugs

## CSS Buggin

## Things I Want To Know More About

- practice with the debugger/sources
- the other tabs under inspect
