# 201_Read_03

- [Learn HTML](#learn-html)
  - [Ordered Lists](#ordered-lists)
  - [Unordered Lists](#unordered-lists)
  - [Answers.1](#answers1)
- [Learn CSS](#learn-css)
  - [The Box Model](#the-box-model)
    - [Inner and Outer Display Types](#inner-and-outer-display-types)
      - [Block and Inline Boxes](#block-and-inline-boxes)
  - [Answers.2](#answers2)
- [Learn JS](#learn-js)
  - [Arrays](#arrays)
  - [Operators and Expressions](#operators-and-expressions)
  - [Conditionals](#conditionals)
  - [Loops](#loops)
  - [Answers.3](#answers3)
- [Things I Want To Know More About](#things-i-want-to-know-more-about)

## Learn HTML

Provides baseline info on cohesion between structure(HTML), design(CSS), and functionality(JavaScript) in regards to websites and the web in general.  
Brief rundown on elements and tags with various [links](https://developer.mozilla.org/en-US/docs/Web/HTML) to dive deeper and explore more specialized topics.

### Ordered Lists

Ordered lists are defined with the `<ol>` tag as the parent and `<li>` as the nested/child tag for individual list items.  
Various attributes can be added to the opening `<ol>` tag, such as:

- `compact` - followed with boolean; deprecated, should use CSS instead to give same styling.
- `start` - gives the ability to change starting number, rather than defaulting to 1, 2, 3, etc.
- `type` or `list-style-type` rule - changes from numbers to other value types like letters or roman numerals (upper/lower).

Able to be nested with `<ul>` or vice versa as needed/desired.  
DOM interface, `HTMLOListElement`

### Unordered Lists

Unordered lists are specified with `<ul>` as the parent element and much like `<ol>`, `<li>` for the list items.

Shares the `compact` attribute like `<ol>` as well as suggestion to use CSS.  
`type` which is also deprecated and replaced with `list-style-type` CSS styling, differs as we are given choice for `circle`, `disc`, `square`, and (if the browser supports it, `triangle`.  

DOM Interface is `HTMLUListElement`.  

### Answers.1

1. When should you use an `unordered list` in your HTML document?
    - When the order of the list items does not matter
2. How do you change the `bullet style` of unordered list items?
    - by using CSS rule `list-style-type`
3. When should you use an `ordered list` vs an `unorder list` in your HTML document?
    - Ordered list for listing out steps or specific order of things, uordered when there is no need for specific order.
4. Describe two ways you can change the numbers on `list items` provided by an ordered list?
    - by using `start` attribute to change starting number or `type` attribute/`list-style-type` rule to change to letters or roman numerals.

## Learn CSS

Tells what CSS is and does.  
Provides [links](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics) for tutorials and challenges.

### The Box Model

The Box Model tells us to think of everything that CSS styles (content, padding, border, and margin) as having box around it and should allow us to better visualize it and therefore have more control over styling. (seen through browser dev tools/inspect element option)

#### Inner and Outer Display Types

##### Block and Inline Boxes

**Outer display** types refers to the behavior of the "box" and how it behaves with it's surroundings (other boxes) and the flow of the site.  
Are values set in the `display` property for inner and outer display types. Is the default setting for behavior.  

- `block` display type boxes break into new lines, dimensions (`width` and `height` are respected), and padding, margin, and border values effect other elements in their placements.
- `inline` display type boxes do not break into new lines, dimensions, padding and borders (top and bottom) do not effect other elements, left and right padding, margin, and borders will effect elements on the same line.
  - `<a>`, `<span>`, `<em>`, and `<strong>` elements use `inline` display type by default.  

**Inner display** type controls how elements are organized within the box, changed through CSS rule of `display: flex;`

### Answers.2

1. Describe the CSS properties of `margin` and `padding` as characters in a story. What is their role in a story titled: “The Box Model”?
    - Padding and Margin, always together, but never in direct contact. The border stands between them. Padding's job is to keep the contents on the inside in place from touching the border, and margin's job is to keep other elements from getting near the border.
2. List and describe the four parts of an HTML elements box as referred to by the `box model`.
    - content is the text or images enclosed within the element, padding is the distance the content is from the border, border makes a perimeter around the content and padding, margin is the distance on the outside from other elements.

## Learn JS

### Arrays

### Operators and Expressions

### Conditionals

### Loops

### Answers.3

1. What `data types` can you store inside of an `array`?
2. Is the `people` array a valid JavaScript array? If so, how can I access the values stored? If not, why?
3. List five shorthand operators for assignment in JavaScript and describe what they do.
4. Read the code below and evaluate the last `expression` and explain what the result would be and why.
5. Describe a real world example of when a conditional statement should be used in a JavaScript program.
6. Give an example of when a `loop` is useful in JavaScript.

## Things I Want To Know More About
