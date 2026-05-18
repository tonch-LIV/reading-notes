# 301_Read_05

- [Thinking in React](#thinking-in-react)
  - [Heirarchy](#hierarchy)
  - ['static' version](#static-shock)
  - [Minimal build](#minimal-and-complete-version)
  - [State](#state-address)
  - [Inverse data flow](#inverse-flow)
  - [Answers.1](#answers1)
- [Higher-Order Functions](#higher-order-functions)
  - [Answers.2](#answers2)

This is important because...  
knowing the thought process behind building React apps with the use of components further solidifies the understanding when actually building them.

## [Thinking in React](https://reactjs.org/docs/thinking-in-react.html)

Building in React breaks down to;  
Building Components,  
Describing the visual states for each component,  
Connecting components together, allowing data to be shared.  

or as five steps,  

1. [Break the UI into component hierarchy](#hierarchy)
2. [Building a 'static' version](#static-shock)
3. [Honing a minimal, complete version of React state](#minimal-and-complete-version)
4. [Identify where state should live](#state-address)
5. [Add inverse data flow](#inverse-flow)

### Hierarchy

Similar to a building a wireframe; components and subcomponents are identified and named.  
Might be useful to think about whether a function, class selector, or similar should be created for the item in question, in regards to separation of concerns.  
Each component should focus on ***ONE*** responsibility.

Well structured JSON files might automatically map to the structure of components and UI, because UI and data models often share similar architecture.  
The hierarchy comes into play when components are contingent on others (and their data).

### 'static' (shock)

A working version built BEFORE adding interactivity, design, and state. Done by building components that reuse other components and pass data using props (data passed from parent to child, without state).  

Can start building "top down" (easiest for simpler projects), or "bottom up" (better for larger projects).  

Once built, the components become a reusable library.

### Minimal and complete version

Knowing that state is needed mainly for;  
variables that change over time,  
are being passed through props,  
being computed from passed down props/state.  

Avoiding unnecessary state avoids things such as;  
duplication,  
synchronization bugs,  
complicated debugging,  
complex architecture and code building.

#### State (address)

One of, if not THE most important React architecture concepts and skills.  
State should live in the closest common parent component that needs it.  

Parent owns state
↓
Passes data through props
↓
Children display/update data

### Inverse flow

Child input to received props from parent, updates the State, even though it is owned by the Parent.  

### Answers.1

1. What is the `single responsibility principle` and how does it apply to components?
    - Component(s) should prioritize doing one thing well vs doing / being in charge of doing many things.
2. What does it mean to build a 'static' version of your application?
    - Having a minimally built application that illustrates structure and hierarchy, without going as far as adding interactivity and/or state.
3. Once you have a static application, what do you need to add?
    - Identify where state should live (closest common parent that will utilize state).
      - functionality and interactivity (event handlers, dynamic behavior)
4. What are the three questions you can ask to determine if something is state?
    - Does it change over time?  
    - is something being passed through props from a parent?
    - Can it be computed in the current props/state?
5. How can you identify where state needs to live?
    - State needs to live in the closest common parent component of the child that needs to use it.

### Answers.2

## [Higher-Order Functions](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK)

1. What is a "higher-order function"?
    - y
2. Explore the `greaterThan` function as defined in the reading. In your own words, what is line 2 of this function doing?
    - 1
3. Explain how either `map` or `reduce` operates, with regards to higher-order functions.
    - 2
