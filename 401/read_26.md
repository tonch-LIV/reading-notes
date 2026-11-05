# 401_Read_26 - Component Based UI / React Refresh

- [React Quick Start](#react-quick-start)
  - [Answers.1](#answers1)
- [Render and Commit](#render-and-commit)
  - [Answers.2](#answers2)
- [Things to Learn More About](#things-to-learn-more-about)

## [React Quick Start](https://react.dev/learn)

A JS library forbuilding UI though resuable components. Each comp. is an individual piece that manages it's portion of the UI.

- **Components**: Reusable functions running JSX.
- **JSX**: Syntax that combines HTML-like markup within JS.
- **Props**: Data that is passed from parent to child components.
- **State**: Data that is remembered by a component and that can be updated using Hooks (`useState`).
- **Conditional redering**: Deciding what appears based on JS conditions.
- **Lists**: Displaying collections of data by using methods like `.map()`.
- **Event handlers**: Functions that execute based on user interaction.

Rather than manually updating *individual* DOM elements; React updates the UI when state changes, and only for the component that changed, not the whole page/site.

### Answers.1

1. What are the building blocks of a React app
    - Components
2. What is the difference between an HTML element and a React component?
    - HTML elements are browser elements.
      - i.e. `<html>`, `<h1>`, `<li>`, etc.
    - React comps. are functions, smaller pieces to the greater project that contain their own logic.
      - i.e. `<Home />`, `<App />`, etc.
3. What is JSX and why do we use it?
    - JavaScriot XML; syntax extension that allows for use of HTML-like markup inside of JS.
    - Keeps UI markup and related JS logic together.
4. Describe the process of embedding JavaScript expressions in JSX.
    - using curly `{}` braces. Allows the rendering of variablke values or other expressions.
    - `<h1>Hello, {name}!</h1>`
5. Does React or JSX have any special features for iteration or conditional logic?
    - no, regular JS is used for iteration and conditionals.
6. How does React know to respond to a user’s inputs?
    - event handlers are used to listen for user interactions and thus execute appropriate functions.
7. What word indicates that a React component manages data with a Hook? How can two react components share data?
    - `use` such as, `useState`; sharing data can happen by 'lifting' or returning state up to the closest parent component and then passing the updated data down as props.

## [Render and Commit](https://react.dev/learn/render-and-commit)

To update the UI, React follows three main steps:  
`Trigger -> Render -> Commit` *(... and finish w/ paint)*  
Otherwise known as 'painting' the updated screen.  

During the **Initial rendering**, React creates the necessary DOM nodes.  
When state is updated, React calculates what the UI should look like so it may **re-render** appropriately.  
React only changes DOM elements when necessary in order to be **effecient** when handling **DOM updates**.  
Once changes are commited and React knows what should be updated and rendered, the browser visually displays the updated interface in a process known as '**painting**'.  

### Answers.2

1. What are the three steps of refreshing a React UI?
    - Trigger - Render is requested by state being updated.
    - Render - Components called by React to calculate the UI that will be displayed.
    - Commit - Necessary DOM changes are applied by React.
2. How do you trigger updates to a component after the initial render?
    - Through state changes / updates; state setter function (`useState`).
3. Does React recreate DOM nodes on every re-render?
    - no, a comparison between new render and previous is made only the updates are changed in the DOM.
4. After React has updated the DOM, what still needs to happen before the user sees the change?
    - Paint, the new render must visually be reflected on screen.

## Bookmark and Review

- [Your First Component](https://react.dev/learn/your-first-component)
  - Creation and nesting of comps.
- [Importing and Exporting Components](https://react.dev/learn/importing-and-exporting-components)
  - Organizing comps. across files.
- [Writing Markup with JSX](https://react.dev/learn/writing-markup-with-jsx)
  - JSX syntax. attributes, and format rules
- [sass cheatsheet](https://devhints.io/sass)
  - Sass variables, nesting, and styling of syntax.
- [react cheatsheet](https://devhints.io/react)
  - JSX, comps. props, and state reference.

## Things to Learn More About

- The three steps when updating UI.
