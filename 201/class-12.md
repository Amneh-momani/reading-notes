#  Chart.js
Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create.

## Creating a Chart
It's easy to get started with Chart.js. All that's required is the script included in your page along with a single < canvas > node to render the chart.


To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. So add this to the body of our HTML page:

     <canvas id="buyers" width="600" height="400"></canvas>


At first sight a < canvas > looks like the < img > element, with the only clear difference being that it doesn't have the src and alt attributes. Indeed, the < canvas > element has only two attributes, width and height. These are both optional and can also be set using DOM properties. When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high. The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.

> **Note** : If your renderings seem distorted, try specifying your width and height attributes explicitly in the < canvas > attributes, and not using CSS.

## Fallback content
The < canvas > element differs from an < img > tag in that, like for < video >, < audio >, or < picture > elements, it is easy to define some fallback content, to be displayed in older browsers not supporting it, like versions of Internet Explorer earlier than version 9 or textual browsers. You should always provide fallback content to be displayed by those browsers.


For example, we could provide a text description of the canvas content or provide a static image of the dynamically rendered content. This can look something like this:

> < canvas id="stockGraph" width="150" height="150">
  current stock price: $3.15 + 0.15
</ canvas>< canvas id="clock" width="150" height="150">
  < img src="images/clock.png" width="150" height="150" alt=""/>
</ canvas>

## Required </ canvas> tag

As a consequence of the way fallback is provided, unlike the < img> element, the < canvas> element requires the closing tag (</ canvas>). If this tag is not present, the rest of the document would be considered the fallback content and wouldn't be displayed.

If fallback content is not needed, a simple < canvas id="foo" ...></ canvas> is fully compatible with all browsers that support canvas at all.

# Drawing shapes with canvas

Before we can start drawing, we need to talk about the canvas grid or coordinate space. Our HTML skeleton from the previous page had a canvas element 150 pixels wide and 150 pixels high. To the right, you see this canvas with the default grid overlayed. Normally 1 unit in the grid corresponds to 1 pixel on the canvas. The origin of this grid is positioned in the top left corner at coordinate (0,0). All elements are placed relative to this origin. So the position of the top left corner of the blue square becomes x pixels from the left and y pixels from the top, at coordinate (x,y). Later in this tutorial we'll see how we can translate the origin to a different position, rotate the grid and even scale it, but for now we'll stick to the default.

## Drawing rectangles

First let's look at the rectangle. There are three functions that draw rectangles on the canvas:

+ fillRect(x, y, width, height)
>Draws a filled rectangle.

+ strokeRect(x, y, width, height)
>Draws a rectangular outline.
+ clearRect(x, y, width, height)
>Clears the specified rectangular area, making it fully transparent.

The fillRect() function draws a large black square 100 pixels on each side. The clearRect() function then erases a 60x60 pixel square from the center, and then strokeRect() is called to create a rectangular outline 50x50 pixels within the cleared square.

In upcoming pages we'll see two alternative methods for clearRect(), and we'll also see how to change the color and stroke style of the rendered shapes.

## Drawing paths

+ beginPath() : Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
+ Path method : Methods to set different paths for objects.
+ closePath() : Adds a straight line to the path, going to the + start of the current sub-path.
+ stroke() : Draws the shape by stroking its outline.
+ fill() : Draws a solid shape by filling the path's content area.


> **Note** : When the current path is empty, such as immediately after calling beginPath(), or on a newly created canvas, the first path construction command is always treated as a moveTo(), regardless of what it actually is. For that reason, you will almost always want to specifically set your starting position after resetting a path.

## Lines
_For drawing straight lines, use the lineTo() method._

### lineTo(x, y)
Draws a line from the current drawing position to the position specified by x and y.
This method takes two arguments, x and y, which are the coordinates of the line's end point. The starting point is dependent on previously drawn paths, where the end point of the previous path is the starting point for the following, etc. The starting point can also be changed by using the moveTo() method.



## Path2D objects

 there can be a series of paths and drawing commands to draw objects onto your canvas. To simplify the code and to improve performance, the **Path2D** object, available in recent versions of browsers, lets you cache or record these drawing commands. You are able to play back your paths quickly.

 ## Colors

Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

color is a string representing a CSS < color >, a gradient object, or a pattern object. We'll look at gradient and pattern objects later. By default, the stroke and fill color are set to black (CSS color value **#000000**).

## Line styles

+ lineWidth = value
+ lineCap = type
+ lineJoin = type
+ miterLimit = value
+ getLineDash()
+ setLineDash(segments)
+ lineDashOffset = value


> Note also that only start and final endpoints of a path are affected: if a path is closed with closePath(), there's no start and final endpoint; instead, all endpoints in the path are connected to their attached previous and next segment using the current setting of the lineJoin style, whose default value is miter, with the effect of automatically extending the outer borders of the connected segments to their intersection point, so that the rendered stroke will exactly cover full pixels centered at each endpoint if those connected segments are horizontal and/or vertical). See the next two sections for demonstrations of these additional line styles.

## Using line dashes
The setLineDash method and the lineDashOffset property specify the dash pattern for lines. The setLineDash method accepts a list of numbers that specifies distances to alternately draw a line and a gap and the lineDashOffset property sets an offset where to start the pattern.


Patterns : In one of the examples on the previous page, we used a series of loops to create a pattern of images. There is, however, a much simpler method: the createPattern() method.


## Drawing text

The canvas rendering context provides two methods to render text:

+ fillText(text, x, y [, maxWidth])

Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
+ strokeText(text, x, y [, maxWidth])

Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

## Styling text

+ **font = value**
The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
+ **textAlign = value**
Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
+ **textBaseline = value**
Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
+ **direction = value**
Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.

In the case you need to obtain more details about the text, the following method allows you to measure it.

**measureText()** 
Returns a TextMetrics object containing the width, in pixels, that the specified text will be when drawn in the current text style.


