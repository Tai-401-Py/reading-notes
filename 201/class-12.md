# Chart.JS

## the Canvas element

`<canvas>` Looks similar to `<img>` Element wioth the only difference being that it only has the height and width attributes.

While the id element and class element arent specific to the `<canvas>` element, they are global and it's a good idea to apply to it for easy identification and styling.

### The Grid

Canvas grid uses coordinate space. normally 1 unit in grid is === 1px on canvas.

Canvas also only supports 2 primitive shapes, rectangles and paths. 

Paths are created and then you can stroke or fill the path to render it. 

You can use lines to create paths and fil in order to create othe shapes suchas triangles.

Using mathematical formulas you can create all sorts of shapes. such as Arcs. 

Using arc() or arcTo() methods you can create more shapes

Context --- 

`arc( x, y, radius, startAngle, endAngle, counterclockwise)`

`arcTo (x1, y1, x2, y2, radius)`

please not that angles in this function are measured in radians not degrees. (Radians = Pi/180 * degrees)

You can also make Bezier and quadratic curves. 

`quadraticCurveTo(cp1x,cp1y, x, y)` - ths draws a line from x to y and uses a control point to establish a curve.

`bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x ,y)` - Biggest difference is the set of two control points.

IMPORTANT! You must close a <canvas> tag otherwise it will think the rest of the document is fallback content. 

The getContext() is a rendering method that needs to be called to so that it has context to draw.

### Make em pretty (colors)

`fillstyle = color` and `strokestyle = color` can be used to change fill and outline colors. They also support the alpha attribute for making diagrams. 

You can use for loops to make some very interesting color variations. using a math formula to calculate out colors. 

`globalAlpha = transparencyValue` (between 1.0 to 0.0 - 1.0 is default)

You can also use line caps
`butt` - Stops at end point
`round` - is a circle that has it's center point stop at destinations
`square` - see round, but it;s square instead. 

you can also use setLineDash and the lineDashOffset property, You can also use this to get marching dotted line effect.

Gradients can also be done in standard and radial. As well as patterns used to repeat.

Drawing text is fairly dtaright forward and comes in two types, `fill/strokeText(text, x, y[, maxWidth]` Text properties share a lot of common ground with CSS.