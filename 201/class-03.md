
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