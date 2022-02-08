
# Readings: Basics of HTML, CSS, and JS

---

## HTML + CSS

---

### Text

- Two different types of markup
  - Structural
    - Elements describe both headings and paragraphs
  - Semantic
    - Provides additional information such as emphasis placement, quotes, acronym meanings.

Headings

- Six different heading levels `<h1-6>`

Paragraphs are self-contained and will appear on new lines with each `<p>` element

Bold and italics can be added inline with `<b>` and `<i>` [^0]

Subscript `<sub>` and Superscripts with `<sup>`

Whitespace in html will only ever display as one space so you can use multiple spaces in order to format code for easier reading.

Linebreaks can also be used in text formatting with `<br />` in order to start a new line.

Horizontal rules can be added with `<hr />` which is useful for extra sepeartion between subjects

### SEMANTIC MARKUP 

---

Semantic markup are text elements not meant to affect structure but add additional information, helpful for screen readers.

Tags such as `<strong>` which bolds text and `<em>` which italicizes.

In quotations you can either use `<blockquote>` which will indent the quotation or `<q>` which will usually put quotes around the element but IE does not read the `<q>` element weel, as such avoid using it. 

Abbreviations and acronyms both use the same element `<abbr title="">` title attribute is used here as well to indicate full terminology. 

Citations `<cite>` are used when referring to the title of a piece of media and Definitions `<dfn>` are used to define a term when you first use it. 

`<address>` element is special in that it is typically used to house contact details about the page author. 

`<ins>` and `<del>` are very handy peices, insert underlines and del strikes to show changes in text or revisions. As an alternative you may also use `<s>` to strike through a word. 

## CSS

---

CSS or "Cascading Style Sheet"

CSS allows you to affect formatting and display of text on a web document. This can either be done in the HTML document using a `<style>` element or through linking an external style sheet.  

CSS Declarations have 3 parts, a selector, a property and a value. 

```css
#selector {
    property: value;
}
```

You can use a `<link href="../../styles.css type="text/css">` to indicate where to find external stylesheets, and link them to your page. 

How things cascade,

1. Rule of first to last - CSS will resolve with the next instance overwriting the first
2. Specificity - will target the more specific the tag.
3. Muy importante! - tag `color: red !important;` - to overwrite any other styling for that element. 

Elements may also be inherited by parent elements, such as anything styled to the `<body>` will likely be added to any child elements nested in it, unless they are given more specific styling. 

## Javascript

---

Statements is an individual instruction which makes up a series. A computer will follow statements one by one.

**NOTE: JavaScript is CASE SENSITIVE** so check your spelling and syntax.

Statements can be organized into blocks, which can be used to organize code for the developer

Don't forget to comment! `//` Comments make things easier to understand for your future self as well as any other person reading your code. 

When writing, don't forget to assign `let "variablenamehere"=` or variables these are values which the computer will remember.

Three main data types - Numeric - String - Boolean

- Numerics are strictly numbers which can contain decimals
- String are made of characters put together
- Boolean or "true/false"

Variables can be done in short hand

```JavaScript
let price = x;
let quantity = y;
  //can also be written 
let price, quantity
price = x;
quantity = y;
  //alternatively
let price= x; quantity = y;
let total = price * quantity;
  //Then use write command to show
let el = document.getElementById('cost');
el.textContext = 'text used to replace';
```

Naming conventions

- Must begin with Letter, $, or _
- Can NEVER use - or . in a variable
- don't use reserved keywords
- They are always CaseSensitive
- Always try and use a name that describes the information it stores.
- Always write variables starting lowercase and Capitalizing every other word soYourVariableLooksLikeThis.

Arrays

- Whenever you need to list items an array is appropriate
  - you don't need to set the number of values an array will hold
  - great for complex data as well
- Values are assigned to an array inside square brackets seperated by commas

```js
let meat;
meat = ['ham', 'pastrami', 'salami']
```

- This example is called an array literal
  - values can also be written on individual lines

```js
let meat = new Array('ham',
                     'pastrami',
                     'salami')
```

- This example is called an array constructor
  - You can use a method called `item()` to retreive data
    - remember computers start counting from 0 so the first index item is item 0.

- Updating array items 

```js
//Updating list item 1
meat [0] = 'turkey';
//get the element with id
let el = document.getElementById('meat');
//replace with second item in array
el.textContent = meat[1];
```

- Expressions rely on operators
  - For sample operators please see [102 Reflection and Discussion 8](../ReflectionandDiscussion08.md)

  