
# Reading: 06 - JS Object Literals, the DOM

---

## Understanding the problem domain

  The real world is messy and many problem domains that will be faced are messy and difficult to comprehend, they may even look totally different to different people.

Once you understand the problem domain, programming becomes easy. As such, understanding is the most important part of writing code.

If you can't understand it, simplify the problem domain, or get better at understanding.

Cutting out cases and honing the area of focus can improve the comprehension of the problem domain.

Build on the small concepts and you can more easily understand a larger problem domain.

Don't fall into the trap of "Enough time talking, let's get to coding". As the better you understand, the quicker you can code, and it's cheaper and more efficeint to get things right the first time around rather than the second.

## The differences between primitive values and object references

Primitive Values and Object references will behave differently. This affects how variable assignments are done.

- Data types in JavaScript
  - Boolean
  - Null
  - Undefined
  - Number
  - BigInt
  - String
  - Symbol
  - Objects
    - Arrays, Functiuons, and DAtes are all just Objects when you look at them closely.

### Differences between Value and Referenece [^0]

Primitive values and objkect references are stored differenty.

When a primitive value is assigned e.g. `let variable = 'one'` the variable is directly set.

When variables are set with an object, things change. That variable now contains a referenece to the object.

[^0]

```JS
const moe = {
  name: 'Moe Szyslak',
  occupation: 'Bartender',
  voicedBy: 'Hank Azaria'
}
```

When executing this code, it creates an objhect and gets stored in the Memory, the variable of `moe` no longer contains the new object directly, it only contains a reference to that memory address. Much like a street address doesn't tell you about the house, but it will tell you where to find the house.

### Mutable and immutable data

- Primitive Values
  - immutable
    - Variable exists in memory and can call to individual letters. But can not change the data of the string itself.
    - One fix is to creat a new string from the old one and reassign the string to the parent variable.
- Object References
  - mutable
    - One such type is arrays (they are really just objects)
    - You can alter them directly, since you can just change the existing data.
      - If you define the variable with `const` you can no longer reassign valuse, but you can still mutate the existing values.

Why does this matter?

Object references do not contain values directly, so when doing absolute `===` they are comparing memory addresses which are different. Rather than content. As such care should be taken when comparing objects.

In order to check contents you need to do one of two things

1. Iterate through an object and check that each key and value match.
This can be tricky because an object’s property can be an object in itself.
2. Convert the object to a suitable primitive before doing the equality check.

## THE DOM (Document Object Model)

the DOM specifies hot the model of an HTML page should be created in a browser.

It's called a Document "Object" Model because the model "tree " is made of objects.

Each object representing different parts of the page loaded in the browser window. Sometimes you will hear the DOM called an API ( Application Programming Interface). APIs let humans and scripts talk to each other, the DOM states what can and can't ask the browser

the DOM tree consists of 4 main types of node.

- The Document Node
  - Start point for all visits to the DOM tree
- Elements Node
  - To access the DOM tree start by looking for elements. ONce you find the one you want, you can then start to access it's attributes adn text.
    - You should start learning how to access this node before the next two
- Attribute Nodes
  - Opening tags of HTML elements can carry attributes and these are represented by attribute nodes in the DOM Tree. 
    - Note that they are not children, they are part of that element.
- Text Nodes
  - Once you've acessed an element node, you can access this node. This is where tesxt is stored. 
  - Text nodes CAN NOT have children (they are sterile).

## Workin' the Tree!

Acessing and updating the DOM Tree involves 2 steps.

1. Locate the node that represents the element you want to work with.
2. Use its Text Content, Child Elements, and Attributes

Step 1: Acessing the Elements
 
- Selecting indiviudal nodes.
  - `getElementById()` - Uses value of an elements id attribute ( should be unique)
  - `querySelector()` Uses CSS Selector and returns first matching element. 
- Select Multiple Elements (Node Lists)


[0^]: Frequently directly quoted from[Better Programming:What’s the Difference Between Primitive Values and Object References in JavaScript?, by Chris Geelhoed](https://betterprogramming.pub/intermediate-javascript-whats-the-difference-between-primitive-values-and-object-references-e863d70677b)
