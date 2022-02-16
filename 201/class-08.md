# CLASS 08 READING JOURNAL: MORE CSS LAYOUTS AND REVIEW

---

## Basics of layout

The basics of Layout come in two forms, things that are inline, or things tha come in a block level. 

Inline items behave like words and sit next to each other on a single line. Typically preserving surrounding whitespace.

Block elements however create thier own new lines, and unless told otherwise will span the full width.

There is also now the display property which is used more frequently for styling options.

setting display property to `display: flex;` makes the box a block level element but now allows flex properties that will control alignment, order, and flow.

There are several ways to align containers through flex and grid formats. allowing you to justify and align in more ways.

- Use flexbox for 1 dimensional layouts
- use grid for more multi-axis layouts

Mix and match to really give your page unique style.

### Additional info for layouts 

Fixed width layouts are handy, and will remain static so you you have more control.

However you can end up with large gaps on the screen, users with high resolution monitors may have a harder time reading, if a user increases font size, text may not fit in the allotted space.

Fluid layouts use percentages, and will expand and contract to fill entire browser space regardless of screen size. Tolerant of larger font sizes because page can stretch.

However. If you don't control width design can look different than intended. Text can get too long on window. if a fixed width item exists it can cause text to overflow a parent element.

## Layout Grids - rehashed

Grids are useful to help control layout and flow of a site.

- Creates continuity between pages. and consisitency in information placement
- Helps predict layouts for collaboration and user interfacing.

- A lot of designers use a 960 px grid. 