# 401_Read_28 - Component Lifecycle / useEffect Hook

- [useEffect hook](#useeffect-hook)
  - [Dependency Array](#dependency-array)
  - [Component's Lifecycle](#components-lifecycle)
  - [Answers.1](#answers1)
- [Boomark and Review](#bookmark-and-review)
- [Things to Learn More About](#things-to-learn-more-about)

## [useEffect hook](https://react.dev/reference/react/useEffect#reference)

`useEffect()` is referred to as a 'Hook' that deals with how React Components synchronize with an external system (network cnnections, APIs, subscriptions; systems that have a lifecycle that needs to stay coordinated with a component).

Rendering should remain pure, `useEffect()` manages its interactions after React commits a render.

**Effects** are fucntions that synchronize components with external systems.  
A **cleanup function** stops or reverses after an effects setup after an completion and if needed.  
**External systems** can include, but are not limited to; APIs, timers, browsers events, and network connections.  

### Dependency Array

A **dependency array** controls when an effect needs to run again.  
Three common patterns are,  

|Syntax|When the effect runs|
|---|---|
|`useEffect(() => {})`|After every committed render|
|`useEffect(() => {}, [])`|On mount, with cleanup on unmount|
|`useEffect(() => {}, [count])`|On mount and whenever count changes|

React *Strict* Mode may also run an additonal setup and cleanup cycle during development to detect mistakes.  

### Component's Lifecycle

Throughout a **component's lifecycle**, a component can,  

- mount (initial render commited),  
- update (re-render after dependencies change),  
- or un-mount (disappear, cleanup is ran).  

Through `useEffect()`, an effect can have its own individual setup-and-cleanup cycle, even while components remain mounted.  

- mount (initial render commited),  
  - ***Effect setup runs (connections, etc.)***,  
- update (re-render after dependencies change),
  - ***Cleanup + new setup(stops previous synch and starts new)***,  
- or un-mount (disappear, cleanup is ran).  

---

After a components setup is when React will run the effects setup.  
If and when dependencies changes; React will run the previous cleanup before running the new setup.  
The cleanup will be ran once again when a component unmounts.  

`useEffect()` is not needed for every state change, only when synching with something external.

### Answers.1

1. What is the main intended use case for the `useEffect` hook?
    - To synchronize a React component with an external system. Allows component to perform operations that need to happen outside normal rendering process.
2. How does the effect’s logic interact with the component?
    - Effect logic is ran after componentncommits its own render.  
    - This allows effect to access component props, state, and interact with external systems.
    - A dependency array determines when the effect should run again (after an initial commit/render) based on changes to specific values.
3. What is the importance of the return value from the effect’s logic function?
    - can return a cleanup function, which stops or undos the synchronization that was performed in setup, before re-rendering or unmounting.

## Bookmark and Review

- [Responding to Events](https://react.dev/learn/responding-to-events)
  - Use of event handlers like `onClick` and `onChange` to respond to user interactions.  
- [Conditional Rendering](https://react.dev/learn/conditional-rendering)
  - Use of `if`, ternary operstors, and `&&` to control what appears in JSX.  
- [Updating Arrays in State](https://react.dev/learn/updating-arrays-in-state)
  - Use of `.map()`, `filter()`, and **spread** syntax to update arrays without mutating (React state should be treated as immutable; do not modify array/object, craete new version and pass to state setter fucntion).  
- [Updating Objects in State](https://react.dev/learn/updating-objects-in-state)
  - Creation of copies of objects instead of modifying state directly.  

## Things to Learn More About

- Effect lifecycle,  
- appropriate use of Effect,  
