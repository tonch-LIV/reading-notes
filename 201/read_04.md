# 201_Read_04

- [Learn HTML](#learn-html)
  - [Creating Hyperlinks](#creating-hyperlinks)
    - [Paths](#paths)
    - [Attributes](#attributes)
  - [Answers.1](#answers1)
- [CSS Layout](#css-layout)
  - [Normal Flow](#normal-flow)
    - [Default Behavior](#default-behavior)
    - [Overriding Normal Flow](#overriding-normal-flow)
  - [Positioning](#positioning)
    - [Static](#static)
    - [Relative](#relative)
    - [Absolute](#absolute)
    - [Fixed](#fixed)
    - [Sticky](#sticky)
  - [Answers.2](#answers2)
- [Learn JS](#learn-js)
  - [Functions](#functions)
    - [Function](#functions)
    - [Where's the Fun(ction) at?](#wheres-the-function-at)
    - [Browser Built-in](#browser-built-in)
    - [Functions vs. Methods](#functions-vs-methods)
    - [Invocation](#invocation)
    - [Parameters](#parameters)
    - [Scope and Conficts](#scope-and-conflicts)
- [Misc.](#misc---6-reasons-for-pair-programming)
- [Things I want to know more about](#things-i-want-to-know-more-about)

This is important because...  

Both positioning and functions, play a vital and crucial role to building well designed sites.

## Learn HTML

Houses links for [tutorials](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content#tutorials_and_challenges) and other challenges.

### Creating Hyperlinks

Without links, there is no web; links connect sites to other sites. URLs (Uniform Resource Locator) can point to HTML files(sites/pages), images, videos, audio, text file, and more. The parts needed to create a link are an `<a>` element with an `href` attribute in the opening tag.

Functionality of links extend to various elements, including block-level ones; only need to wrap the desired link with an `<a>` element. The addition of a `title` attribute (usually after the `href`) allows additional text to show up when the cursor hovers over the mouse, where the dev may add a description or provide context about what's to come should they click/activate the link, not really an "accessibility" inclusion as screen readers or navigating through keyboard strokes might not be able to invoke the "hover".

More information on how requests for sites are made with the use of [web servers](https://developer.mozilla.org/en-US/docs/Learn_web_development/Howto/Web_mechanics/What_is_a_web_server) and what web servers are.

#### Paths

- If linked files are in the same directory, only the file name needs to be specified as the url path or a simple `./` to provide clarity as to where the file is coming from (same directory).
- If the linked file is within a sub directory of the same main directory, you would specify the directory name followed by a forward slash as such, `subdirectory/filename.ext` for the url.
- If we are moving up a directory level (moving up), you would start the url path with `..` followed by the directory you want to go into and then file name as follows, `../sisterDirectory/filename.ext`. The `..` indicates the directory name one level up, no need to name it, only name a directory if you are going into a new one after moving up and searching for a file there. The path name can become very complicated as these syntaxes can be compounded to get to the right place.
- To link straight to the relative directory, without the need to specify how many levels (directories, `..`) up you are moving, you may name just reference the root and start the path name at the "parent" directory, `/parentDirectoryFileIsLocatedIn/fileName.ext`. the `/` at the beginning tells it to start the search at the root directory and proceed from there, rather than the current directory the file being linked from and then moving up.
  - note: all these past examples are for local files, relative to ones individual repo and will break if you move files (either linked or linking / origin > destination) to a different location; this last example continues to work if you move the LINKING file however.
  - Absolute path - The complete path taken from the root to reach the file.
  - Relative path - The path from the current file you are linking from.

#### Attributes

- The same way we link to headings (`#` after the file name), we can use the `#` to link to an element with a corresponding `id` or `href` in it's opening tag.
- the `download` attribute provides a default save name for the file when linking to a download.
- by using the `target` attribute and setting it to "_blank", it points the browser to open the link clicked on in a new tab, rather than on the same page.
- email links are created using the `<a>` element, with an `href` attribute, and `mailto:` followed by the email address within the `href` attribute. Leaving `mailto:` blank opens a equally blank, new outgoing email window from which you may add the info as the user wishes.

### Answers.1

1. To create a basic link, we wrap text or other content inside what element?
    - `<a>` or anchor tag.
2. The href attribute contains what information?
    - the link/location to the link, same page or external; url.
3. What are some ways we can ensure links on our pages are accessible to all readers?
    - descriptive text in plain text, or in titles, bolds, italics.

## CSS Layout

Landing page for tutorials and [challenges](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout)

Having the layout in mind when designing a page allows one as a developer to control the positioning and be prepared for how different elements will interact with each other, different resolutions, and window sizes.

### [Normal Flow](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Introduction)

#### Default Behavior

- If no CSS characteristics have been applied to change behavior, normal flow is the default. Ensuring that elements and content displayed on a site are easily readable, before modifying, is a good starting point.
- Block-level elements adjust the dimensions as needed per the content that it is holding and fills the available inline space of the parent element it is in. It occupies its own line and makes new elements after it, start on a new line.
- Inline-level elements only take up as mush room as the content requires and accommodates other elements within that same line (unless their isn't space left within the parent element, in which case they do move into a new line).
- By using CSS, you may make inline elements behave like block-level elements through the property-value pair of `display: block;` or `display: inline-block`.
  - Margin collapsing - when two elements' margins are touching, it forces the smaller of the two unto a new line.

#### Overriding Normal Flow

Methods to override normal flow are as follows,

- Changing the `display` property - values include `block`, `inline`, `inline-block`.
  - `grid` or `flexbox`
- `float` - allows `block` elements (`<p>`, `<img>`, etc.) to wrap around other elements.
- `position` - control where boxes are placed in relation to other boxes.
  - `static` - default
  - `fixed` - keeps "box" in same spot in viewport.

### [Positioning](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Positioning)

Changes the behavior of elements by taking them out of normal flow, expands on overriding, through the use of the `position` property in CSS.  

#### Static

Default, every element begins with. no need to state/define/write out in CSS, but looks like `position: static;` within CSS rule.

#### Relative

We define `relative` as the value for the `position` property, then expand on it (and the following positions henceforth) with the `top`, `bottom`, `left`, and `right` properties.  
For `relative`, think opposite of the property you define. As in, if define `top`, it will be pushed down by the measurement specified, or pushed from the "top". `left`, it will pushed to the right or pushed from the "left", and so on.

#### Absolute

Again defined as the value for the `position` property. `absolute` elements no loger exist within the normal flow, the space they once took is tken/filled in by the surrounfing elements and it sits within its own layer.  
Think in terms of pop-ups, dialogue boxes, etc.

The way this value moves the element is the "opposite" of `relative`, in a way. The units of measurement dictate the distance the element should sit from the parent elements sides.  

- (postioned element's win over non-positioned elements.)  

Z-index refres to z-axis and controls the "stacking" order of the elements. The higher/ positive value, the more to the top/background; the lower/negative value, the more to the background.

#### Fixed

Places the element relative to the viewport of the browser; very similar to absoulte (relative to the nearest ancestor element).  

Persistent elements in same location, regardless of where you scroll or go on the site.

```css
selector {
    position: fixed;
    top: 0;
```

The above CSS snippet makes the `<h1>` element stick to the top of the screen and removes it form normal flow.

#### Sticky

Combination of `relative` and `fixed`. Element is positioned relatively to a certain point, then becomes `fixed`.  

Think moving Row headers that become superceeded by relevant headers per section.

### Answers.2

1. What is meant by “normal flow”?
    - default positioning and styling; before CSS.
2. What are a few differences between block-level and inline elements?
    - Block - takes full width of line and starts on new line. `<p>`, `<h#>`.
    - Inline - places elements side-by-side, not new line; content only takes up space. `<a>`, `<span>`, `<strong>`.
3. ___ positioning is the default for every html element.
    - Static, stays in normal flow; not affected by top, left, bottom.
4. Name a few advantages to using absolute positioning on an element.
    - useful for overlays, tool tips; collapsible menu '|||' (rotated 90 deg).
    - displays over other content as you scroll; think, layered.
5. What is a key difference between fixed positioning and absolute positioning?
    - Absolute = moves with the page or its container. In relation to parent element. Removed from normal flow. defaults to `<body>` for relative.
      - "place where I want!"
    - Fixed = stays fixed to the screen (viewport) when you scroll. "goes where you go".
      -Relative - ...

## [Learn JS](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting)

Landing page with links to tutorials and [challenges](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting#prerequisites) aimed at teaching the essentials and provide foundation for further learning.

### Functions

A storage mechanism for code that does a single task, which you may invoke and use at a later time.

#### Where's the Fun(ction) at?

Everywhere. They're used to make developing easier and keeping developers sane (..attempt).

#### Browser Built-in

Functions can be used to manipulate,

- Text - through the use of `replace()`
- Arrays - `join()` to combine contents in array into single array.
- Numbers - `random()` to create random numbers

Many are built-in and ready to use, even though they might not be written in javascript (C++/lower level language browser is built on or through APIs).

#### Functions vs. Methods

Functions are methods, when written to be part of an object.  
Custom functions are just that, functions written specifically for the task at hand.  

#### Invocation

The process of running the actual function is called, invoking. To invoke a function, you specify the function name followed by a pair of parentheses (and any arguments, if appropriate), then a semi-colon.  

Being able to call other functions within a function (should they be globally accessible) is a trait.  

#### Parameters

Not all functions do, but there some that require parameters to be specified in order to complete it's job. parameters go within the parentheses. There are also functions that expect a parameter(s) to be specified, but when they aren't; they adopt a default behavior.

#### Anonymous & Arrow

Anonymous functions have no name and expect a function to be its parameter (function expression).  

- `addEventlistener()` - runs code after an event/action from the user.

Rather than using the `function` keyword; arrow functions are specified through the use of `=>`.

#### Scope and Conflicts

To avoid conflicting variable names and possible malicious actions from external scripts; two separate scopes exist. The local scope that says, variable defined within a function can only be recalled within that specific function call. The global scope is from where you may pull from throughout the entire script and within other functions. Local can called upon from only that instance, global can be called from every instance.

- (avoid using `var` as it can mess with the scope considerations.)

### Answers.3

1. Describe the difference between a function declaration and a function invocation.
    - declaring involves outlining what code will be run; invocating is the actual process of running it when called.
2. What is the difference between a parameter and an argument?
    - parameter - a placeholder; usually a variable that will fill in where input with contents of variable
    - argument - an actual value plugged in for the function;

## Misc. - 6 Reasons for Pair Programming

1. Pick 2 benefits to pair programming and reflect on how these benefits could help you on your coding journey.
    - collaboration allows peer review, feedback, different perspectives/styles to merge, allows opportunity to improve code quality and production efficiency

## Things I want to know more about

- Positioning and best use case scenarios
- function manipulation
