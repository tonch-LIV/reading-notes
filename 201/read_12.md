# 201_Read_12

- [JavaScript Canvas](#javascript-canvas)
  - [Rendering Content](#rendering-content)
    - [2D Context](#rendering-content)
  - [Answers.1](#answers1)
- [Chart.js](#chartjs)
  - [Answers.2](#answers2)
- [Animated Charts](#animated-charts)
  - [Line](#line-chart)
  - [Pie](#pie-chart)
  - [Bar](#bar-chart)
  - [Answers.3](#answers3)
- [Drawing Shapes - Canvas](#drawing-shapes---canvas)
- [Styles & Colors - Canvas API](#styles--colors---canvas-api)
- [Text - Canvas API](#text---canvas-api)
- [Things I Want To Know More About](#things-i-want-to-know-more-about)

This is important because...  
adding charts is a good tool to use and incorporate into the the structure of a website to enage the users attention and break up blocks of text and raw data when present.  
Knowing how to add charts is equally important, becasue then we are given the knowledge to modify and customize charts as needed.

## [JavaScript Canvas](https://www.javascripttutorial.net/web-apis/javascript-canvas/)

`<canvas>` is a feature of HTML5 that allows one to draw 2D graphics through the use of JavaScript.  

```html
<canvas width="300" height="300" id="canvas">fallback content</canvas>
```

It requires two attribute, `width` and `height`, which are accessible / able to be modified through DOM properties like other elements.  

```js
const canvas = document.querySelector('#canvas');
const width = canvas.width;  // 300
const height = canvas.height;  // 300
//
canvas.width = 400;
canvas.height = 400;
```

Although rare to find a browser that does not offer support for the `<canvas>` element; if used on a browser that does not, any content within the element tags will be considered fallback content and will display to the user (see earlier example).

### Rendering Content

`<canvas>` is blank until used to access context to draw/display on file; done through the `getContext()` method.  

First the element/id must be selected, then we pass one argument to access the 'drawing content' style of choice through `getContext()`.  

```js
let canvas = document.querySelector('#canvas');
// why not `getElementById()`??  

let ctx = main.getContext('2d');  
// is the variable/property meant to be main or canvas??
// is this meant to be refrencing the `main` element on the page? if so, why select the `#canvas` id?
```

#### 2D Context

Think `x` and `y` axis; bottom right of a 4 quadrant, positive and negative chart.  
Top left is `(0, 0)`. Normally the `y` value, as it grows, would get 'smaller' in negative terms, but since there is no negative; the value defaults to positive integer.

### Answers.1

1. What does the `<canvas>` allow a developer to achieve?
    - Draw 2D graphs using javascript; holds a variety of data/visuals.
2. What is the importance of the closing `</canvas>` tag?
    - not self closing; if browser doesn’t support the `<canvas>` element, content within element is fallback content that will display, most modern browsers support element; needed to avoid rendering/layout issues.
3. Explain what the `getContext()` method does.
    - one argument defines type of content; tells browser what kind of visual you'll represent from data.

## [Chart.js](https://www.chartjs.org/docs/latest/)

The most popular of the charting libraries hosted on [Github](https://github.com/chartjs/Chart.js) and available through [npm](https://www.npmjs.com/package/chart.js) (JavaScript package manager; subsidiary of GitHub, central to JavaScript community).  

Incorporating a chart through Chart.js is as easy as can be thanks to sets of frequently used chart types, plug-ins, and various other customization settings and options being easily available and accessible.  
Includes a strong, actively developed and maintained community backbone with plenty of documentation to learn plenty about anything.  
Chart.js works well and adapts to large datasets, reduces toll taken on DOM tree when rendering canvas, in comparison to other methods like SVG rendering.

### Answers.2

1. What is Chart.js and how it can be brought into your project?
    - most popular (per GitHub), provides many commonly used styles and types of charts plus other features; directly with built-in typings compatible with js or through external packages.
    - Library of ready set tools to build clean visual data representations.
    - chart.js, CDN, added in `script` element on top of page, can be downloaded.
2. List 3 different Chart types you can create using Chart.js.
    - area, bar, and line.

## [Animated Charts](https://webdesignerdepot.com/easily-create-stunning-animated-charts-with-chart-js/)

Superior method to visually display data over raw datasets, regardless of table stylings done. Much easier and faster at representing data trends visually.  

Chart.js simplifies the creation process. A method of linking to working fileset is through direct download and then linking in `<head>` element through `<script>` element.  

`<canvas>` element is added to html file with `id`, `width`, `height` attributes so Chart.js knows where chart will generate.

### Line Chart  

```html
<canvas id="lineChart" width="600" height="400"></canvas>
```

(**from here, reading includes JS through `<script>` tags within html, but can also / should also be done through external JS file.**)  

A variable is created that will contain the linked `id`, as well as the context for what kind of chart will be created (2D, Line).  

```js
var lineChart = document.getElementById('lineChart').getContext('2d');
new Chart(lineChart).Line(buyerData);
```

We continue with creating/plugging in the data. This example will use an object containing labels and the dataset. This object's placement will go above our previous variable.

```js
var lineData = {
 labels : ["January","February","March","April","May","June"],
 datasets : [
  {
   fillColor : "rgba(172,194,132,0.4)",
   strokeColor : "#ACC26D",
   pointColor : "#fff",
   pointStrokeColor : "#9DB86D",
   data : [203,156,99,251,305,247]
  }
 ]
}
```

### Pie Chart

Similar steps are taken for a pie chart; only swapping in  
`new Chart(countries).Pie(pieData, pieOptions);` rather than `.Line` and the dataset definition as well as the options for the chart,  

```js
var pieData = [
 {
  value: 20,
  color:"#878BB6"
 },
 {
  value : 40,
  color : "#4ACAB4"
 },
 {
  value : 10,
  color : "#FF8153"
 },
 {
  value : 30,
  color : "#FFEA88"
 }
];

var pieOptions = {
 segmentShowStroke : false,     // remove stroke from segments
 animateScale : true       //  animate scale of pie so it zooms out from nothing
}
```

### Bar Chart

As for a bar chart; similarities are shared with a line chart. Although, again we define `.Bar` in  
`var income = document.getElementById("income").getContext("2d");
new Chart(income).Bar(barData);`.  
The data set definitions is largely the same,  

```js
var barData = {
 labels : ["January","February","March","April","May","June"],
 datasets : [
  {
   fillColor : "#48A497",
   strokeColor : "#48A4D1",
   data : [456,479,324,569,702,600]
  },
  {
   fillColor : "rgba(73,188,170,0.4)",
   strokeColor : "rgba(72,174,209,0.4)",
   data : [364,504,605,400,345,320]
  }

 ]
}
```

**Plenty more examples and options to choose and learn from founf in the [documentation](https://www.chartjs.org/docs/).**

### Answers.3

1. What are some advantages to displaying data via a chart over a table?
    - visually easier to look at illustration rather than number data set.
2. How could Chart.js aid your previously created applications visually?
    - its a plugin that enables easy creation of all kinds of charts/graphs.
    - in fish bicuits, trends could be observed on days most sold and which location sells the most.

## [Drawing Shapes - Canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

## [Styles & Colors - Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)

## [Text - Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)

## Things I Want To Know More About

- chart options
- declaration / definition structure
