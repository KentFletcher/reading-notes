# Creating Animated Charts with Chart.js
- Charts are far better for displaying data visually than tables.   They are easier to look at and pass along data quickly.
- Chart.js is a JavaScript plugin that uses HTML5's canvas element to draw graphs onto the page easily.
  - You can create bar charts, line charts, pie charts and more.
  - Chart.js is simple to use and very flexible.
- In HTML the `<canvas>` element looks like the `<img>` element, but it does not have the src and alt attributes.  It only carries the width and height attributes, which are optional and can be set using the DOM properties.  The default setting for width is 300 pixels and height is 150 pixels.  There are also ways to size the element with in CSS, but that can be tricky.  It is good practice to set the id attribute because it makes it easier to identify it in a script.
- The `<canvas>` element differs from an `<img>` tag in that, like for `<video>`, `<audio>`, or `<picture>` elements, it is easy to define some fallback content, to be displayed in older browsers not supporting it, like versions of Internet Explorer earlier than version 9 or textual browsers. You should always provide fallback content to be displayed by those browsers.
- The `<canvas>` element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown.
- The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it. The `<canvas>` element has a method called getContext(), used to obtain the rendering context and its drawing functions. getContext() takes one parameter, the type of context. 
- `<canvas>` only supports two primitive shapes: rectangles and paths (lists of points connected by lines). All other shapes must be created by combining one or more paths.
  - There are three functions that draw rectangles on the canvas:
    1. fillRect(x, y, width, height)
      - Draws a filled rectangle.
    1. strokeRect(x, y, width, height)
      - Draws a rectangular outline.
    1. clearRect(x, y, width, height)
      - Clears the specified rectangular area, making it fully transparent.
    - Each of these three functions takes the same parameters. x and y specify the position on the canvas (relative to the origin) of the top-left corner of the rectangle. width and height provide the rectangle's size.
  - A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. A path, or even a subpath, can be closed. To make shapes using paths, we take some extra steps:
    1. First, you create the path.
    1. Then you use drawing commands to draw into the path.
    1. Once the path has been created, you can stroke or fill the path to render it.
    These are the functions used to perform these steps:
    1. beginPath()
      - Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
      - The first step to create a path is to call the beginPath(). Internally, paths are stored as a list of sub-paths (lines, arcs, etc) which together form a shape. Every time this method is called, the list is reset and we can start drawing new shapes.
    1. Path methods
      - Methods to set different paths for objects.
      - The second step is calling the methods that actually specify the paths to be drawn. We'll see these shortly.
    1. closePath()
      - Adds a straight line to the path, going to the start of the current sub-path.
      - The third, and an optional step, is to call closePath(). This method tries to close the shape by drawing a straight line from the current point to the start. If the shape has already been closed or there's only one point in the list, this function does nothing.
    1. stroke()
      - Draws the shape by stroking its outline.
    1. fill()
      - Draws a solid shape by filling the path's content area.
- **Moving the pen**- One very useful function, which doesn't actually draw anything but becomes part of the path list described above, is the moveTo() function. You can probably best think of this as lifting a pen or pencil from one spot on a piece of paper and placing it on the next.
- **Lines**- For drawing straight lines, use the lineTo() method.
  -lineTo(x, y)
  -Draws a line from the current drawing position to the position specified by x and y.
  -This method takes two arguments, x and y, which are the coordinates of the line's end point. The starting point is dependent on previously drawn paths, where the end point of the previous path is the starting point for the following, etc. The starting point can also be changed by using the moveTo() method.
- **Arcs**- To draw arcs or circles, we use the arc() or arcTo() methods.
  - arc(x, y, radius, startAngle, endAngle, anticlockwise)
  - Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by anticlockwise (defaulting to clockwise).
  - arcTo(x1, y1, x2, y2, radius)
  - Draws an arc with the given control points and radius, connected to the previous point by a straight line.
  - The arc method which takes six parameters: x and y are the coordinates of the center of the circle on which the arc should be drawn. radius is self-explanatory. The startAngle and endAngle parameters define the start and end points of the arc in radians, along the curve of the circle. These are measured from the x axis. The anticlockwise parameter is a Boolean value which, when true, draws the arc anticlockwise; otherwise, the arc is drawn clockwise.
- **Bezier and quadratic curves**- These are available in both cubic and quadratic varieties. These are generally used to draw complex organic shapes.
  - quadraticCurveTo(cp1x, cp1y, x, y)
  - Draws a quadratic Bézier curve from the current pen position to the end point specified by x and y, using the control point specified by cp1x and cp1y.
  - bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)
  - Draws a cubic Bézier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y).
  - The difference between these can best be described using the image on the right. A quadratic Bézier curve has a start and an end point (blue dots) and just one control point (indicated by the red dot) while a cubic Bézier curve uses two control points.
  - The x and y parameters in both of these methods are the coordinates of the end point. cp1x and cp1y are the coordinates of the first control point, and cp2x and cp2y are the coordinates of the second control point.
- **Rectangles**- In addition to the three methods we saw in Drawing rectangles, which draw rectangular shapes directly to the canvas, there's also the rect() method, which adds a rectangular path to a currently open path.
  - rect(x, y, width, height)
  - Draws a rectangle whose top-left corner is specified by (x, y) with the specified width and height.
  - Before this method is executed, the moveTo() method is automatically called with the parameters (x,y). In other words, the current pen position is automatically reset to the default coordinates.

- **Colors**- If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.
  - fillStyle = color
    - Sets the style used when filling shapes.
  - strokeStyle = color
    - Sets the style for shapes' outlines.

- **Line styles**- There are several properties which allow us to style lines:
  - lineWidth = value
    - Sets the width of lines drawn in the future.
  - lineCap = type
    - Sets the appearance of the ends of lines.
  - lineJoin = type
    - Sets the appearance of the "corners" where lines meet.
  - miterLimit = value
    - Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.
  - getLineDash()
    - Returns the current line dash pattern array containing an even number of non-negative numbers.
  - setLineDash(segments)
    - Sets the current line dash pattern.
  - lineDashOffset = value
    - Specifies where to start a dash array on a line.

-  **Drawing text**- The canvas rendering context provides two methods to render text:
  - fillText(text, x, y [, maxWidth])
    - Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
  - strokeText(text, x, y [, maxWidth])
    - Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.
- Styling Text- There are some more properties which let you adjust the way the text gets displayed on the canvas:
  - font = value
    - The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
  - textAlign = value
    - Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
  - textBaseline = value
    - Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
  - direction = value
    - Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.