### Charts.JS API 

Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create.

A great way to get started with charts is with Chart.js, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page. It’s a well documented plugin that makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy.
```
The <canvas> element
<canvas id="tutorial" width="150" height="150"></canvas>

At first sight a <canvas> looks like the <img> element, with the only clear difference being that it doesn't have the src and alt attributes. Indeed, 
the <canvas> element has only two attributes, width and height. These are both optional and can also be set using DOM properties.
When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high.
The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS
sizing doesn't respect the ratio of the initial canvas, it will appear distorted.


The <canvas> element differs from an <img> tag in that, like for <video>, <audio>, or <picture> elements, it is easy to define some fallback content,
to be displayed in older browsers not supporting it, like versions of Internet Explorer earlier than version 9 or textual browsers. 
You should always provide fallback content to be displayed by those browsers.

Providing fallback content is very straightforward: just insert the alternate content inside the <canvas> element.
Browsers that don't support <canvas> will ignore the container and render the fallback content inside it.
Browsers that do support <canvas> will ignore the content inside the container, and just render the canvas normally.

<canvas id="stockGraph" width="150" height="150">
  current stock price: $3.15 + 0.15
</canvas>

<canvas id="clock" width="150" height="150">
  <img src="images/clock.png" width="150" height="150" alt=""/>
</canvas>

```
# Drawing rectangles

 There are three functions that draw rectangles on the canvas:

fillRect(x, y, width, height)
Draws a filled rectangle.
strokeRect(x, y, width, height)
Draws a rectangular outline.
clearRect(x, y, width, height)
Clears the specified rectangular area, making it fully transparent.

# Drawing paths
+ beginPath()
Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
Path methods
Methods to set different paths for objects.

+ closePath()
Adds a straight line to the path, going to the start of the current sub-path.
+ stroke()
Draws the shape by stroking its outline.
+ fill()
Draws a solid shape by filling the path's content area.

# Drawing a triangle
For example, the code for drawing a triangle would look something like this:
```
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    ctx.beginPath();
    ctx.moveTo(75, 50);
    ctx.lineTo(100, 75);
    ctx.lineTo(100, 25);
    ctx.fill();
  }
}
```

# Colors
Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

fillStyle = color
Sets the style used when filling shapes.
strokeStyle = color
Sets the style for shapes' outlines.

