# 201_Read_01

- [Getting Started](#getting-started)
  - [Website Design and Process](#website-design-and-process)
  - [JavaScript Basics](#javascript-basics)
  - [Answers.1](#answers1)
- [Intro to HTML](#intro-to-html)
  - [Document Structure](#document-structure)
  - [Metadata](#metadata)
  - [Answers.2](#answers2)
- [Miscellaneous](#miscellaneous)
  - [Designing a site](#designing-a-site)
  - [Semantics](#semantics)
  - [What is JavaScript?](#what-is-javascript)

## Getting Started

This topic matters because its important to know not only how to do something (build a site), but also why the site is being built.  

[Links](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Your_first_website) to various tutorials, such as:

- [Plannning the layout of a website](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Your_first_website/What_will_your_website_look_like) -  
It's important to have a vision or goal of how you want the website to look, so you have something to strive for as you build it.

- [Adding the Content](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Your_first_website/Creating_the_content) -  
How to use HTML to add structure as you incorporate elements and add content.

- [Styling](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Your_first_website/Styling_the_content) -  
How to use CSS to add flair, color, and design elements to the structure (HTML).

- [Interactive elements](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Your_first_website/Adding_interactivity) -  
For the user to be able to engage with the site, create input, and receive output; we use JavaScript.

- [Publishing](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Your_first_website/Publishing_your_website) -  
Like a book, once you polish the content, its format, and are ready to share with others; you make it public and allow others to find it if you are looking for.

### How the Web Works

Restaurant analogy, uses similar terms although used differently.

- **Client** - The computer, terminal, whatever the vehicle interfacing with the network/server. You making the food order.
- **Server** - the chef, the one that has the dishes you are going to order and eat.
- **Network Connection** - This would be the waiter/waitress, they are the connection between client and server, whether it be wired, wireless, optical, nfc, etc.
- **TCP/IP** - The language between you, waiter, and server. you communicate with each other about the plates, portions, ingredients and other requests.
- **DNS** - The names of the dishes vs just listing out ingredients, measurements, recipe, etc.
- **HTTP** - This would tie in TCP/IP and DNS; all three are protocols and coexist in the OSI / DoD model; in our analogy, HTTP would be like the portion size or taste profile of the dish we've ordered... HTTPS would be like cooking at home where you know the recipe is safe and no one tampered with it.
- **Misc. files** - This would be all the other stuff that make the restaurant what it is and sets it apart from all the other restaurants like it; decor, reputation, theme, menu, you name it (CSS, JS, content, etc.).

#### Quick run through

1. When you got to a restaurant, you either view the menu or know what you want. You speak with the wait staff and tell them the name of the dish. This is you ***speaking the same language (TCP/IP)*** through your ***network connection*** while typing the ***URL/name*** of the site into the search bar.
2. The waiter takes your order and relays to the chef. the chef knows the recipe just by name of the dish. This is the ***chef resolving a DNS query*** from the client through the network connection. ***Included*** in the order is the ***HTTP request***.
3. The chef ***approves*** the ***order***, cooks it, and ***starts sending*** out the ***courses*** (apps, entree, etc) through the waiter to the client.
4. ***Client receives*** order and eats.

#### Networking terms explained (view definitions in ___A+/N+_link_here)

**DNS** - Domain Name System  
**Packets** - Layer 3  
**[HTTP](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Web_standards/How_the_web_works#http_basics)** - HyperText Transfer Protocol; GET, HTTP/2 200

### Website Design and Process

Make a plan before starting to build.

- What is your website **about**?
- What **information** are you presenting on the subject?
- What does your website **look** like?

Pen and paper are a combo that has been tested through time and can come in handy here. Sketch a rough idea for how you'd like the layout of the site to be.  
Choose a background color/theme palette. Choose some images. Choose a font.

### JavaScript Basics

JavaScript essentially uses values/elements already on the page, does some sort of operation with those values, then returns an output depending on what the operation was, and that result itself can also be used later on if needed in another operation.

### Answers.1

1. Compose a short poem describing how HTTP sends data between computers.

    >"Clients pick up the phone to make a call,  
    >“Hey Server, send your page and all!”  
    >Through a Network Connection, off it goes,  
    >Riding on TCP/IP boats.  
    >
    >A stop by DNS to say,  
    >“Where does that Server live today?”  
    >Then Packets, small and neat,  
    >Carry data down the street.  
    >
    >The HTTP message replies, polite and plain,  
    >“Please send index.html again.”  
    >The Server smiles, “Here you are!”  
    >And sends it back from afar.  
    >
    >So every page you click to see,  
    >Travels the world, digitally."  

2. Describe how HTML, CSS, and JS files are “parsed” in the browser.
    - First, HTML is downloaded/received from server.  
    - CSS is found and loaded.  
    - CSS and HTML combine and layout of site is rebuilt.  
    - JavaScript comes in and adds functionality
3. How can you find images to add to a Website?
    - Images can be found and added locally by linking local path or by by linking to external site where it's hosted.
4. How do you create a String vs a Number in JavaScript?
    - Strings are surrounded by quotes ('5' or "83"), ; Numbers are standalone, no quotes.
5. What is a Variable and why are they important in JavaScript?
    - Variables are shorthand names given to blocks of code, strings of text, or references to be used later throughtout the file in various places.

## Intro to HTML

HTML is the structure, the skeletal frame of a website. Through the use of semantics, you know what use the content is for and where it should go.

### Getting Started with HTML

An HTML element consists of an opening tag, attribute(s) (if needed), content, closing tag (if called for). HTML offers a basic outline, it is up to the developer how intricate and detailed the site should be; as it pertains to the goal/mission/purpose of the site.

Elements can be placed within each other (nested).
Elements that don't follow the basic outline of opening tag, content, closing tag are referred to as **void** elements and "close" within the opening tag, with or without the closing forward slash `/` (varies per html to xml compatibility).

Attributes are compounded onto elements and modify the contents of the element.

### Document Structure

`<header>` - Thin section across the top of the page with logo and or heading. Can also be used within `<article>` or `<section>`.  
`<nav>` - Links to additional pages, also remains atop of the page.  
`<main>` - contains most of the important content of the page. Should be used once per page and within the `<body>`.  
`<article>` - section of content that's related to the main content, but can stand on its's own.  
`<section>` - groups together a single part of a website, in relation to its contents.  
`<footer>` - Thin section across the bottom of the page, known to contain copyright, notices, contact info, and the sort.  

non-semantic elements exist for when you as the developer want to group items together that fall into other semantic elements.  
`<div>` - block level  
`<span>` - inline  

Line break `<br>`, can be used nested within `<p>` elements to maintain a firm structure.  
Horizontal rule `<hr>` adds a dividing line; used outside elements.  

#### Information Architecture

Past planning the layout and structure of a single webpage, is to consider how one would approach structuring a website with multiple pages.  

1. It is good to keep in mind which elements will remain consistent across the various number of pages, such as:
    - Header
        - Title and Logo
        - Site Language selector
    - Navigation Menu
    - Footer
        - Copyright notice
        - Link to terms and conditions, contact info, and accessibility policy
2. Then, back to pen(pencil?) and paper. Sketch a rough draft with no major detail or content to have an ide of the layout of major stuff.
3. Make a list of all other elements that will be local to each individual page.
4. Sort and organize into groups or how they will be divided in similar pages.
5. Sketch a sitemap, which will show the flow/navigation between each page.

### Metadata

Metadata is information located in the `<head>` of the HTML file and contains information that is not displayed on the main content are of the browser when the page is loaded.  

Elements found in the `<head>` range from the page `<title>`, `<meta>` for adding context, linking to CSS `<link>` or JavaScript `<script>` (although standard practice to put JS link in the footer or with `defer` attribute to allow HTML to load before JS.), or setting the language of the site.

### Answers.2

1. What is an HTML attribute?
    - An attribute is added information added to an element, specifically in the opening tag.
2. Describe the anatomy of an HTML element.
    - An element consist of opening tag, attribute (if needed), content, and closing tag (if called for).
3. What is the difference between `<article>` and `<section>` element tags?
    - `<article>` can stand on its own, but stiil related to main content ;`<section>` groups together parts of a site per relevance.
4. What elements does a “typical” website include?
    - includes `<html>`, `<head>`, `<body>`, `<main>`, `<header>`, `<footer>`, plus a few others
5. How does metadata influence Search Engine Optimization?
    - Influences SEO by
6. How is the `<meta>` HTML tag used when specifying metadata?
    - Used to add context, whether specifying language, character set, or linking to CSS/JS.

## Miscellaneous

### Designing a site

1. What is the first step to designing a Website?
    - Figure out the goal of making a website will be.
2. What is the most important question to answer when designing a Website?
    - What are you hoping to accomplish?

### Semantics

1. Why should you use an `<h1>` element over a `<span>` element to display a top level heading?
    - It is implied that an `<h1>` tag will format the content as a top level heading, where as a `<span>` is catered for more general use.
2. What are the benefits of using semantic tags in our HTML?
    - A semantic element gives the text it wraps around the meaning of what it will do.

### What is JavaScript?

1. Describe 2 things that require JavaScript in the Browser?
    - Defined running order and Browser APIs
2. How can you add JavaScript to an HTML document?
    - `<script>` element

## Things I want to know more about
