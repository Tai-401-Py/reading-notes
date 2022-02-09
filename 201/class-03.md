
# HTML Lists, Control Flow with JS, and the CSS Box Model

---

## HTML Lists

Can be nested using the following syntax
```html
<ul>
  <li></li>
  <li>
    <ul>
        <li></li>
    </ul>  
  </li>
</ul>
```


### Ordered lists

- Lists in which each item are numbered, or systematically lettered; used for steps, or for documents in which sections need to be referenced.
  - Created with `<ol>` tag with `<li>` tags nested in it.
  - Type attributes can be assigned and type of ordering changed.[^0]


### Unordered lists

- Lists that start with a symbol rather than an alphanumeric character
  - Created with `<ul>` tag with `<li>` tags nested in it.
  - Type attributes can be added to change symbols. [^0]

### Definition lists

- Lists that typically consist of a series of terms and definitons
  - Created with `<dl>`  with `<dt> (definition term)`  tags and `<dd> (definition)` nested in it.
  - Sometimes two `<dd>` tags will be under a single `<dt>` tag. For multiple definitions of the same term. 

[^0]: It is preferred that you use CSS `list-style-type` property.

---

## BOXES

---

CSS treats all HTML as if they were boxes and there are properties you can assign to change how these boxes look and interact.

- By default a box is sized to be jus tas big as it's content.
- Most often resized using percentages or pixels.
  - Pixels tend to be more popular because of absolute size
- Percentages it's always relative to browser window size.

- Page designs can be made to change sizes based on users screen as such they use the `min-width` and `max-width` attributes

- Limiting height using `min-height` and `max-height` can also be helpful, but be wary of overflow that can be caused by not enough room for content.

- Overflow can be controlled two different ways.
  - `overflow: hidden;` which will hide any excess
  - `overflow: scroll;` which will give a scroll bar.

- Borders have several different attributes that can adjust width, style, and color.
  - `border: width style color;`
  - Images can also be used
    - `'webkit'-border-image: url("")`
      - Attributes that can be assigned.
        - stretch
        - round
        - repeat
  - Border radius can be used to round out borders

- Margins control the space between border and content of box.
  - Can also be written short hand, see borders for ex.

- Display property allows you to change inline to block, and block to inline style elements.

- Blocks can also be hidden or visible to show/hide the element
  - If box is set to hidden, the whole element will not show.


## JavaScript

### Truthy and Falsey Values

- Truthy values are treated as if they are true.

|value|Description|
|---|---|
|let a = true;| Traditional Boolean True|
|let a = 1;| Numbers other than 0|
|let a = 'bone';| String with content|
|let a = 10/5;| Number calculations|
|let a = 'true'| True written as string|
|let a = '0'| Zero as a string|
|let a = 'false'| false as a string|

- presence of object or array can be condiered truthy.
  - unary operator returns results if truthy will run, if false second operation will run.

Note: NaN == NaN is still boolean false because the value is undefinable therfore always boolean false.

- Short circuit values
  - Logical operators processed L -> R and will stop as soon as they resolve, returning the value that stopped the processing.
  - Value may be returned truthy or falsey although not boolean
  - because of short circuiting programmers will often put the most likely to be true statement first in OR operations, and inverse for AND operations.

### Loops!

Loops are fun! They will continue to check and run until condition returns false. 

3 types.

1. For Loop
  - If you need to run something a specific amount of times
2. While Loop
  - If you don't know how many times to run a thing, great for lists.
3. Do While Loop
  - Similar to while loop, but will always run at least once even if valuse is false. 

Loops can be very helpful when dealing with arrays, especially if you want to run the same code for the items in the arrays.

Note: Browsers will continue to run the JS and wont stop till it is finished, in the case of infinite loops, you could cause a memory overflow and crash. BEWARE THE OUROBOROS! 

FOR LOOP

- often used to loop through array items, as long as the counter variable is less than the number of items in array it will run as set. `( i = 0; i < arrayLength; i++>)`

WHILE LOOP

- Often used when you don't know how many items are going to be in an array. It will continue to run as long as the statement is true.

DO WHILE

- See WHILE LOOP - except it will always run at least once even if statement is false(y)
