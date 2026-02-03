# 201_Read_02

- [Intro to HTML](#intro-to-html)
  - [Text Fundamentals](#text-fundamentals)
  - [Adv. Text Formatting](#adv-text-formatting)
- [Learn CSS](#learn-css)
  - [How is CSS structured](#how-is-css-structured)
- [Learn JS](#learn-js)
  - [JavaScript basics](#javascript-basics)
  - [Making decisions in code - conditionals](#making-decisions-in-code---conditionals)
- [Review - git commits](#review---git-commits)
- [Things I want to know more about](#things-i-want-to-know-more-about)

## Intro to HTML

[Links](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content) to tutorials and challenges.

### Text Fundamentals

Headings and paragraphs exist in most pieces of writing and exist to give readable content structure and be able to easily discern different sections of what is being read.  

Paragraphs are wrapped in `<p>` elements.  
Headings stand out by being wrapped in `<h#>` elements. Replacing the number sign (#) with the corresponding number (1-6).  

Having a structured site allows the user to easily scan the page for relevant content. Also, useful for search indexes to be able to pull content and categorize important keywords. Increasingly helpful for screen readers and accessibility software. Useful when utilizing CSS/JS to target specific elements.  

Semantics are key to have, as their inclusion allows a developer to know what an element is expected to do/output. Easier on the developer as well as it saves keystrokes for not having to style individual/generic elements (`<span>` or `<div>`) to match desired styling/format.

### Adv. Text Formatting

Blockquotes are specified by using the `<blockquote>` element and citing the source with the `cite` attribute.  
Inline quotes are done very similar, they however use the `<q>` element within the parent element, whereas the `<blockquote>` element is the parent element. Also citing as an attribute in the opening tag.  

`<abbr>` is used to represent abbreviations or acronyms.  

To represent contact information, the `<address>` element is used to wrap content.  

Superscript and subscript is represented by `<sup>` and `<sub>` respectively.

Time and date is specified with the `<time>` element.

Various elements can be used to represent computer code, such as:

- `<code>` - for generic snippets.
- `<pre>` - retains text format as seen in text editor, keeps indents, line breaks, and other whitespace.
- `<var>` - used for variable names.
- `<kbd>` - for input entered into PC.
- `<samp>` - for the output of a computer program.

1. Why is it important to use semantic elements in our HTML?
    - Important to use semantics to have an idea what the code will be used for, for accessibility compatibility and ease of use, and to make the developers life easier.
2. How many levels of headings are there in HTML?
    - 6 levels of headings, try not to use them all and keep the hierarchy order in mind when using.
3. What are some uses for the `<sup>` and `<sub>` elements?
    - Formulas, numbers, dates, math in general.
4. When using the `<abbr>` element, what attribute must be added to provide the full expansion of the term?
    - `title`.

## Learn CSS

### How is CSS structured

CSS can be used one of three ways. Best practice is to link an external `.css` file within `<head>` element using th `<link>` element, but you may also choose to write out all the rules used on that one page in the `<head>` element with the `<style>` element. Last choice is if you want to style just one, single element, you may choose to style it by using the `<style>` attribute in the opening tag. A benefit of linking an external style sheet is that one sheet can be used for multiple pages, if need be.  

Various selectors exist that dictate which HTML element will be style, such as:

- `*` - Universal, everything on the HTML file will be styled with the following rule.
- `(specific element)` - style all elements of the same type (paragraphs, headings, etc.).
- `.class_name` - elements with specific `<class>` attribute will be style appropriately, adding unique name after period.
- styling based on location in file or state of element.

Functions can also be used in CSS rules to further add and modify the styling of an element/selector.  

Shorthand properties save keystrokes as they allow to set various values within one line.  

1. What are ways we can apply CSS to our HTML?
    - Linking externally, writing internally or inline.
2. Why should we avoid using inline styles?
    - Bad practice and makes editing more difficult.
3. Review the block of code below and answer the following questions:
    - What is representing the selector?
        - `<h2>`
    - Which components are the CSS declarations?
        - the code inside`{}`, `color: black;` is one declaration and `padding: 5px;` is the second declaration.
    - Which components are considered properties?
        - the characteristic that is going to edited. `color` or `padding`.

## Learn JS

### JavaScript basics

1. What data type is a sequence of text enclosed in single quote marks?
2. List 4 types of JavaScript operators.
3. Describe a real world Problem you could solve with a Function.

### Making decisions in code - conditionals

1. An `if` statement checks a __ and if it evaluates to ___, then the code block will execute.
2. What is the use of an `else if`?
3. List 3 different types of comparison operators.
4. What is the difference between the logical operator `&&` and `||`?

## Review - git commits

[This topic matters because]

## Things I want to know more about
