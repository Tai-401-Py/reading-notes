
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

##