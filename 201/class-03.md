
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
  - `overflow: scroll;` which will give a scroll bar 

- Borders have several different attributes that can adjust width, style, and color.
  - `border: width style color;`
  - Images can also be used
    - `'webkit'-border-image: url("")`
      - Attributes that can be assigned 
        - stretch
        - round
        - repeat
  - Border radius can be used to round out borders

- Margins control the space between border and content of box.
  - Can also be written short hand, see borders for ex.

- Display property allows you to change inline to block, and block to inline style elements. 

- Blocks can also be hidden or visible to show/hide the element
  - If box is set to hidden, the whole element will not show.
