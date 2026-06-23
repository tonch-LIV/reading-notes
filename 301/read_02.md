# 301_Read_02 - State & Props

- [React Lifecycle](#react-lifecycle)
  - [Mounting](#mounting)
  - [Updating](#updating)
  - [Unmounting](#unmounting)
  - [Components and Methods](#components-and-methods)
  - [Answers.1](#answers1)
- [React State vs. Props](#react-state-vs-props)
  - [State](#state)
  - [Props](#props)
  - [Answers.2](#answers2)
  - [Things I Want to know More About](#things-i-want-to-know-more-about)

This is important because..
as a developer, it's vital to know how to be able to store data and handle changes. Learning the abstract layer process gives insight into the innerworkings.

## [React Lifecycle](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

Components can be defined as either `classes` or `functions`; lifecycle events are methods that are used within them and can allow you to update the UI and app states.  
The three general phases of a lifecycle are **Mounting**, **Updating**, and **Unmounting**.  

### Mounting

The stage for when instances of components are being created and inserted in the DOM.  
`constructor` and `render` happen here, as does ***`componentDidMount`***, ***static getDerivedStateFromProps***, and ***UNSAFE_componentWillMount***.

### Updating

Updating (re-render) happens only and only when a component is updated or a state changes.  
The order in which this occurs is as follows;  

***static getDerivedStateFromProps***,  
***shouldComponentUpdate***,  
***render***,  
***getSnapshotBeforeUpdate***,  
***componentDidUpdate***,  
***UNSAFE_componentWillUpdate***,  
***UNSAFE_componentWillReceiveProps***

### Unmounting

This is the final phase and it is called when a component is being removed from the DOM.  
The only lifecycle event to occur within this phase is ***componentWillUnmount***.

### Components and Methods

**constructor()**  
A React component that is called before being mounted, as a subclass component; super(props) should be called, lest the props be undefined.  
State can be assigned through constructors using `this.state` or by `eventHandler` binding to instances.  
Use of `this.setState()` should be avoided as it is unnecessary and can cause side effects, such as ignoring any update to props.  

**static getDerivedStateFromProps()**  
A method used when state relies on changes in props *over time*, a rare occasion.

**render()**  
Render will examine `this.props` and `this.state` when called. The render function/method should not modify the component state, nor should it interact directly with the browser to avoid re-rendering and bugs that could occur therein. Class components require render, it is a must.  
If **shouldComponentUpdate()** returnsa false, render will no be invoked/called.  

**componentDidMount()**  
A method called as soon as a component is mounted. Anything loaded through a network request or to initialize the DOM should occur here and subsequently, can be unloaded in **componentWillUnmount()**. Used lightly, `setState()` can be called here, but will cause a re-render and may impact performance.  

**shouldComponentUpdate()**  
Components re-render whenever a state changes; setting the `shouldComponentUpdate()` to false gives one the ability to prevent this behavior from happening manually, with the side benefit of optimizing performance. Other components rely on `shouldComponentUpdate` and its answer when invoked.  

**getSnapshotBeforeUpdate()**  
Captures pic of DOM before changing anything on it; rarely used.

**componentDidUpdate()**  
Performs network requests after change.

**componenetWillUnmount()**  
Cleans up DOM and network requests.  

**UNSAFE events**  
Deprecated events that lead to bugs and unintended side effects. Some have up to date replacements.  
componentWillMount > **ComponentDidMount**  
componentWillReceiveProps > **static getDerivedStateFromProps**  
componentWillUpdate > **getSnapshotBeforeUpdate**  

### Answers.1

1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
    - `render` phase, before the commit phase; within Mounting.
      - UI is built.
      - Mounted to DOM.
      - componentDidMount is run.
2. What is the very first thing to happen in the lifecycle of React?
    - `constructor()` is invoked.
      - `state` initialized & bindings happen.
3. Put the following things in the order that they happen: `componentDidMount`, `render`, `constructor`, `componentWillUnmount`, `React Updates`?
    - `constructor`
    - `render`
    - `React Updates`
    - `componentDidMount`
    - `componentWillUnmount`
4. What does `componentDidMount` do?
    - components are created > network request made > inserted into DOM.
      - APIcalls, timers, adding event listeners.

## [React State vs. Props](https://www.youtube.com/watch?v=IYvD9oBCuJI)

React manages data and re-renders on changes.

### State

Data handled & updated inside component.

### Props

~ Arguments to function.  
Data passed into component; updated outside.  
What you want component to initialize/render to.

### Answers.2

1. What types of things can you pass in the props?
    - almost anything.
      - strings, numbers, booleans, arrays, objects, functions (event handlers).
2. What is the big difference between props and state?
    - State is handled and updates data internally (in component)(for dynamic data).
      - props receive data(updated) from a parent component(read-only); don't update/modify data.
3. When do we re-render our application?
    - Whenever a change happens to state (or props).
4. What are some examples of things that we could store in state?
    - counter state, Forms (input elements), API data, UI state.

## Bookmark and Review

- React Docs
  - [State and Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)
    - data that changes over time and changes what is displayed, is state.
    - setting state
      - `this.state = { count: 0 };`
    - updating state
      - `this.setState({ count: this.state.count + 1 });`
    - avoid 'hardcoding'
      - `this.state.count = 5;`
  - [handling events](https://reactjs.org/docs/handling-events.html)
    - events trigger updates.
    - user action > event > state change > re-render
  - [‘Developer Tools’ Tutorial](https://reactjs.org/tutorial/tutorial.html)
    - a shared parent should be used to manage all states instead of individually.
    - Components are kept in sync and keeps logic together.
- [React Bootstrap Documentation](https://react-bootstrap.github.io/)
  - Bootstrap components for React.
  - keeps focus on logic rather than styling from scratch.
    - Prebuilt UI components.
    - Responsive design.
    - Faster development.
- [Boootstrap Cheatsheet](https://getbootstrap.com/docs/5.0/examples/cheatsheet/)
  - speeds up styling
    - Layout → `container`, `row`, `col`
    - Spacing → `mt-3`, `p-2`
    - Colors → `bg-dark`, `text-light`
- [Bootstrap Shuffle](https://bootstrapshuffle.com/classes)
  - used to search and discover Bootstrap classes and use correct classes.
- [Netlify](https://www.netlify.com/)
  - deploys frontend apps on web.
  - useful for simple deployment, continuous integration, and free hosting tier.
    - push to GitHub
    - netlify builds
    - app goes live

## Things I Want to Know More About

- state vs props example.
- bedsides errors; why some components are `UNSAFE`/deprecated.
