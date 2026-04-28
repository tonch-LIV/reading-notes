# 301_Read_01

- [Component-Based Architecture](#component-based-architecture)
  - [Answers.1](#answers1)
- [Props in React](#props-in-react)
  - [Answers.2](#answers2)
- [Bookmark / Review](#bookmark--review)
- [Things I Want To Know More About](#things-i-want-to-know-more-about)

This is important because...  

## [Component-Based Architecture](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm)

A method of segmenting a project into smaller, more manageable logical pieces. Component reusability is a vital part of component based architecture, as it combines functionality with repeated use cases (reduces time in development; increases reliability).  
Recognized standard component frameworks include, but not limited to; COM/DCOM, JavaBean, EJB, COBRA, .NET, web / grid services.

### Components

Components are modular, replaceable, and reusable software objects that are constructed ahead of time with the intention of working with other components.  
Software components may be defined as a 'unit of composition'.  

Below is an example of a components structure, with a component being plugged inside.  
Note that the `Product` component must be imported first before being used. The syntax to invoke/plug the component becomes `<Product />`.  
`App` itself becomes a component we can later reuse and we allow this by opening the door through `export`.

```js
import Product from "./Product"

function App() {
  return (
      <div>
          <h1>PRODUCTS</h1>
          <div className="App">
              <Product />
          </div>
      </div>
  )
}

export default App
```

***Source***: [freeCodeCamp](https://www.freecodecamp.org/news/how-to-use-props-in-reactjs/#:~:text=parent%20component)

The three different views of a component are as follows; object-oriented view, conventional view, and process-related view.

**Object-oriented view**  
Multiple components working together as part of cooperating class(es). Problem domain and infrastructure class(es) (analysis, design; respectively), identify tributes and operations of the current implementation; interface definition that allow classes to communicate and cooperate..

**Conventional view**  
Components are seen as parts (elements, module, etc.) brought together and adapted to fit into something bigger; their encompassing logic, internal structure for logic to be processed, and interface that allows functionality and data processing.

**Process-related view**  
Components are built from system library based on the context

#### Characteristics

Reusability - designed to be re-used across situations / applications, but can be task-specific.
Replaceable - interchangeable with other similar components.
Extensible - functionality/structure can be expanded upon original scope.
Encapsulated - code block is contained within itself and rarely depend on other components.

### Design Principles

> "The design of data structures, interfaces, and algorithms should conform to well-established guidelines to help us avoid the introduction of errors."  - [tutorialspoint](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm#:~:text=The%20design%20of%20data%20structures%2C%20interfaces%2C%20and%20algorithms%20should%20conform%20to%20well%2Destablished%20guidelines%20to%20help%20us%20avoid%20the%20introduction%20of%20errors)

### Answers.1

1. What is a “component”?
    - (class) a small piece of code (javascript, html) that is reusable that produces UI elements; accepts input.
    - an interchangeable, re-usable block of code.
2. What are the characteristics of a component?
    - Independent / Contained (works on it's own)
    - Reusable
    - Scalable / Composable
    - Accepts input / manages state
    - Interchangeable
    - Expandable
3. What are the advantages of using component-based architecture?
    - (class) organization (cleaner code, maintanence), reusable (saves time, less errors, scalable).
    - reliable, easier development and deployment, reusable, maintainable and upgradeable.
(Optional). Disadvantages
    - May become complex managing many components.
    - Requires planning and design upfront.

## [Props in React](https://www.freecodecamp.org/news/how-to-use-props-in-reactjs/)

###

### Answers.2

1. What is “props” short for?
        -
2. How are props used in React?
        -
3. What is the flow of props?
        -

## Bookmark / Review

- ["Passing Data through Props" React Tutorial](https://reactjs.org/tutorial/tutorial.html)
- React Docs
  - [Hello World](https://reactjs.org/docs/hello-world.html)
  - [Introducing JSX](https://reactjs.org/docs/introducing-jsx.html)
  - [Rendering Elements](https://reactjs.org/docs/rendering-elements.html)
  - [Components and Props](https://reactjs.org/docs/components-and-props.html)

## Things I Want To Know More About
