
# HTML LINK, JS FUNCTIONS, INTRO TO CSS LAYOUT

---

## HTML

### LINKS

- Links are created using the `<a>` element. You specify destination with the `<href>` tag. 
  - Text in between the `<a>` tags is the display text.
- On larger sites it is reccomended that you put each individual HTML page in a child directory. 

- When linking E-mail the href is followed by `mailto:address@site.com` 
- You can force a new window with the `target="_blank"` attribute.
- Using id tags it's possiblew to link to the same part of the same page you're in. 
-To link to a psecific part of another page you would input the destination URL with the ID tag of the portion you want to address to. 

## CSS

### Layout

- CSS treats each HTML element as it's own little box.
  - These elements willl either be block level (seperate line) or inline (same line) elements.
- When one block-level element is inside another it's a parent/containing element.

- Element positions
  - Normal Flow
    - Every block-element on a new line.
  - Relative positioning
    - Shifts element top, right, bottom, or left, of where it would have been placed.
- Absolute Positioning
  This postiions the element ir relation to it's containing element. It's taken out of normal workflow, meaning it doesn't affect anything else. 
- Fixed Positioning
  This is a form of absoulte positioning. It positions in realtion to browser window.
- Floating Element
  Element is also out of normal workflow. It becomes a block level element that everything can flow around.

There is also a property called `z-index` which allows you to control the box on top. 

Clearing Float 

- The clear property allows you to say that nothing in the same element should touch the left or right side of the box.

Parents of floated elements problem - If containing element only contains floating elements it is treated as 0px tall.

Parents of floated elements solution - Developers get around the problem by adding an extra element after last floated box inside the containing element. Setting the clear property to `clear: both;`.
  
- Not really reccomended because then an extra null element is created.

More recently it has been adopted to instead have a CSS based solution of setting `overflow: auto;` and `width: 100%;`. 

Many webpages with multiple columns in thier design make use of the float element. Setting `width` `float` and `margin` attributes.

Note reccomended use class attribute  `<class="columnXofY">` to float and adjust each individual block element. 

### Screen Sizes

Be aware that you may be dealing with many different screen sizes. 

The higher the resolution the smaller the text appears to be.

Most web designers try to create pages from 960-1000px as a standard. As well as fit the main info of a page in the first 570-600px in height. As this is what most users can see.

### Fixed Layout

Fixed width layouts are handy, and will remain static so you you have more control.

However you can end up with large gaps on the screen, users with high resolution monitors may have a harder time reading, if a user increases font size, text may not fit in the allotted space.

### Fluid Layout

Pages use percentages, and will expand and contract to fill entire browser space regardless of screen size. Tolerant of larger font sizes because page can stretch.

However. If you don't control width design can look different than intended. Text can get too long on window. if a fixed width item exists it can cause text to overflow a parent element. 

### Layout Grids

Grids are useful to help control layout and flow of a site. 

- Creates continuity between pages. and consisitency in information placement
- Helps predict layouts
for collaboration and user interfacing.

- A lot of designers use a 960 px grid 

### Multiple Style Sheets

Some web page authors use multiple style sheets in order to control layout and flow better, using multiple to control, layout, typiography, borders, tables etc... 

Note: style sheets are loaded from top down.

## JavaScript

### FUNCTIONS!

Functions group a series of statements together to perform a specific task. Packaged in a code block. 

- Pieces of important info passed to the function are called paramenters. 

Declaring a Function

```JS
function yourFunction(){
  codeblockgoeshere
}
//Use this to call back to function
yourFunction();
```

Sometimes you need to get parameters from something.

```JS
function getParameter(x, y){
  //return function here is used to calculate the total of x, y times
  let total = x * y;
  return total;
}
//you can now call the function and manually input variables to output the return/
let totalOne = getParameter(3, 5) //will run function using 3 and 5 as x and y)

```

You can also use this method to retunr an array wiuth multiple indexes.

```JS
function getParameter(x, y, z){
  //return function here is used to calculate the total of x, y times
  let calcOne = x * y;
  let calcTwo = x * y * z;
  let total = [calcOne, calcTwo]
  return total;
}
//you can now call the function and manually input variables to output the return/
let totalOne = getParameter(3, 5, 3)[0]; //will set array index [0] to the result of totalOne
let totalTwo = 
```

Local vs Global Variable.

Local Variables are created in a function and only work within their own function.

Global variables created outside of a function function anywhere. It helps to declare vglobal variables so that they will function across your functions if you plan on reusing them. 

## REsons for pair programming

PAir programming involves two partiesm a driver and a navigator. NAvigator directs the driver with no direct input and thinks about the big puicture. The Driver handles the mechanics of coding and puts the code on page.

4 KEY THINGS WHEN LEARNING NEW LANGUAGE

- Listening - hearing and interpretation of vocab
- Speaking - unsing correct grammar and vocab
- Reading - understanding written language
- Writing - producing from scratch meaningful well structured solutions.

During paired sessions be sure to work on these key skills.

Reasons to pair.
1. Greater Efficiency
  - Creates higher quality code and catches more bugs in first iteration saving time on debugging.
2. Engaged Collab
  - Body doubling is more engaging and it's harder to get off track.
  - Relying on each other you can often find a solution. 
3. Learning from peers.
  - Learning from peers can expose you to techniques you may have not thought of.
4. Improves Social Skills
  - Paior programming helps develop communication skills to find the correct words to convey thought when grabbing a keyboard isn't an option.
5. Job interview readiness
  - Pair programming between an applicant and employee is not an uncommon practice for hiring. They will carry out exercises to check compatibility and collaboration. These are often more important than technical skills.
6. Work environment readiness
  - Most companies utilize pair programming to onboard fresh staff, knowing how to means one less hurdle to overcome in training.