# Read12
##  Chart.js
- Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create.
- A great way to get started with charts is with Chart.js, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page. It’s a well documented plugin that makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy.
- Setting :
The first thing we need to do is download Chart.js. Copy the Chart.min.js out of the unzipped folder and into the directory you’ll be working in. Then create a new html page and import the script:
![chart1](img/chart01.png)
- Drawing a line chart:
To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which [Chart.js](https://www.chartjs.org/docs/latest/getting-started/) can draw our chart. So add this to the body of our HTML page.
- It's easy to get started with Chart.js. All that's required is the script included in your page along with a single < canvas> node to render the chart.
- we need to write a script that will retrieve the context of the canvas, so add this to the foot of your body element.
![chart2](img/chart02.png)
- pass some options to the chart via the Line method or Inside the same script tags we need to create our data.

[ArticleSource](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

<hr>

## Canvas

- < canvas> looks like the < img> element, with the only clear difference being that it doesn't have the src and alt attributes. Indeed, the < canvas> element has only two attributes, width and height. These are both optional and can also be set using DOM properties.
- When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high.
- The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.
- Providing fallback content is very straightforward: just insert the alternate content inside the < canvas> element. Browsers that don't support < canvas> will ignore the container and render the fallback content inside it. Browsers that do support < canvas> will ignore the content inside the container, and just render the canvas normally.
- The fallback content is displayed in browsers which do not support < canvas>. Scripts can also check for support programmatically by testing for the presence of the getContext() method. 
[ArticleSource1](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)

- the canvas grid or coordinate space. Our HTML skeleton from the previous page had a canvas element 150 pixels wide and 150 pixels high.see this canvas with the default grid overlayed. Normally 1 unit in the grid corresponds to 1 pixel on the canvas. The origin of this grid is positioned in the top left corner at coordinate (0,0). All elements are placed relative to this origin. So the position of the top left corner of the blue square becomes x pixels from the left and y pixels from the top, at coordinate (x,y). Later in this tutorial we'll see how we can translate the origin to a different position, rotate the grid and even scale it, but for now we'll stick to the default.
![grid](img/grid.png)

- < canvas> only supports two primitive shapes: rectangles and paths (lists of points connected by lines). All other shapes must be created by combining one or more paths. Luckily, we have an assortment of path drawing functions which make it possible to compose very complex shapes.

- the rectangle: There are three functions that draw rectangles on the canvas:
1. (x, y, width, height)
Draws a filled rectangle.
2. strokeRect(x, y, width, height)
Draws a rectangular outline.
3. clearRect(x, y, width, height)
Clears the specified rectangular area, making it fully transparent.
Each of these three functions takes the same parameters. x and y specify the position on the canvas (relative to the origin) of the top-left corner of the rectangle. width and height provide the rectangle's size. 
-  A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. A path, or even a subpath, can be closed. To make shapes using paths, we take some extra steps:

1. beginPath(): Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
2. Path methods: Methods to set different paths for objects.
3. closePath(): Adds a straight line to the path, going to the start of the current sub-path.
4. stroke(): Draws the shape by stroking its outline.
5. fill(): Draws a solid shape by filling the path's content area.
- call the beginPath(). Internally, paths are stored as a list of sub-paths (lines, arcs, etc) which together form a shape. Every time this method is called, the list is reset and we can start drawing new shapes.
[ArticleSource2](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)
- Apply colors to a shape, there are two important properties we can use:
1. fillStyle = color
Sets the style used when filling shapes.
2. strokeStyle = color
Sets the style for shapes' outlines.
- globalAlpha = transparencyValue
Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.
#### Line styles
There are several properties which allow us to style lines: 

1. lineWidth = value
Sets the width of lines drawn in the future.
2. lineCap = type
Sets the appearance of the ends of lines.
3. lineJoin = type
Sets the appearance of the "corners" where lines meet.
4. miterLimit = value
Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.
5. getLineDash()
Returns the current line dash pattern array containing an even number of non-negative numbers.
setLineDash(segments)
Sets the current line dash pattern.
6. lineDashOffset = value
Specifies where to start a dash array on a line.
[ArticleSource3](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)

- The canvas rendering context provides two methods to render text:

1. fillText(text, x, y [, maxWidth]): Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
2. strokeText(text, x, y [, maxWidth]): Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

[ArticleSource4](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)