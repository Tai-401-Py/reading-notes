# Reading 14 b

## What google learned about teams

### Project Aristotle

Looking at the data amongst many different groups of peers it didn't matter if two teams had many similar points of data they worked differently.

While looking into this data they came across research studies into "group norms". Which govern a group and the unwritten rules about how they operate. These rules can significantly change how individuals operate once they arte in a group setting.

It was here they found the key to greating a better group. However one group norm was not good for another group, but made one group many times more sucesful. Once they began to research this, they found that any particular team that did well on one assignment was likely to do well on others.

A few things stood out though. Teaks that spoke equally amongst members were much more cohesive. Teams that also had high social sensitivity also performed very well.  

Creating a safe social environment is also very important to building a strong effective team. Without trust and safety people feel guarded and aren't able to perform because there is always something holding them back.

## CSS Transforms and Animations

### Transform Syntax

Transform accepts a handful of values.

- rotate (deg)
- scale (0.00) this can be done on x, y axis with (0.00, 0.00)
- translate (measurement here) this can also be done on x,y (x, y)
- skew (xDeg, yDeg)
- perspective (measurement) - creates a vanishing point. Thisa can also be done on x, y, and z axis by adding the rotate(X,Y,Z) attributes.  

- `transform-style: preserve-3d` can be used when nesting an item in an already transformed object.
- `backface-visibility` hidden; make the opposite side of an image invisible.

You can walso string to apply transformations

### Transitions

For best compatability use vendor prefixes across all instances of your css when applying transitions or amnimations.

Not all properties can be transtioned. Only those with a halfway point.

- background-color
- background-position
- border-color
- border-width
- border-spacing
- bottom
- clip
- color
- crop
- font-size
- font-weight
- height
- left
- letter-spacing
- line-height
- margin
- max-height
- max-width
- min-height
- min-width
- opacity
- outline-color
- outline-offset
- outline-width
- padding
- right
- text-indent
- text-shadow
- top
- vertical-align
- visibility
- width
- word-spacing
- z-index

- `transition-duration:` typically put in (s) or (ms)
- `transition-timing:` 
  - linear
  - ease-in
  - ease-out
  - ease-in-out
- `transition delay:` each timing seperated by a comma will affect the nest item in sequence for transition.

sometimes all oit takes is some simple interactivity to really wow your users. 