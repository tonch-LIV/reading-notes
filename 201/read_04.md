# 201_Read_04

- [Learn HTML](#learn-html)
  - [Creating Hyperlinks](#creating-hyperlinks)
    - [Paths](#paths)
    - [Attributes](#attributes)
    - [Answers.1](#answers1)
- [CSS Layout](#css-layout)
  - [Normal Flow](#normal-flow)
  - [Positioning](#positioning)
- [Learn JS](#learn-js)
  - [Functions](#functions)
- [Misc.](#misc---6-reasons-for-pair-programming)
- [Things I want to know more about](#things-i-want-to-know-more-about)

This is important because...  

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

#### Answers.1

1. To create a basic link, we wrap text or other content inside what element?
    - `<a>` or anchor tag.
2. The href attribute contains what information?
    - the link/location to the link, same page or external; url.
3. What are some ways we can ensure links on our pages are accessible to all readers?
    - descriptive text in plain text, or in titles, bolds, italics.

## CSS Layout

### Normal Flow

### Positioning

1. What is meant by “normal flow”?
2. What are a few differences between block-level and inline elements?
3. ___ positioning is the default for every html element.
4. Name a few advantages to using absolute positioning on an element.
5. What is a key difference between fixed positioning and absolute positioning?

## Learn JS

### Functions

1. Describe the difference between a function declaration and a function invocation.
2. What is the difference between a parameter and an argument?

## Misc. - 6 Reasons for Pair Programming

1. Pick 2 benefits to pair programming and reflect on how these benefits could help you on your coding journey.

## Things I want to know more about
