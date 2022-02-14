
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
  - `getElementsByClassName()` - Selects all elements that have a specific class attribute.
  - `getElementsByTagName()` - Selects all elements with specific tag names
  - `querySelectorAll()` Uses CSS Selector to nab all matching elements.
- Traversing Nodes
  - `parentNode` Selects the parent of the current element node (will only return 1 element)
  - `previous/nextSibling` Selects the previous or next Sibling from the tree. 
  - `first/lastChild` Select the first or last child of the current Element.

Step 2: Work with those Elements

- Access/Update text Nodes
  - `nodeValue` This property lets you access or update contents of a text node.
  - `innerHTML` Allows you to access child elements and text content 
  - `textContent` Allows you to just access the Text
- Several methods let you create/remove nodes (Called DOM tree Manipulation)
  - `createElement()`
  - `createTextNode()`
  - `append/removeChild()`
- Access or Update Attribute Values
  - `hasAttribute()` - checks for attribute
  - `getAttribute()` - get the attribute value
  - `setAttribute()` - update value
  - `removeAttribute()` - remove attribute

## Caching DOM queries

Methods that find elements are called DOM queries. When you need to work with elements multiple times it helps to assign a variable to them.

When a script selects and element, the interpreter must locate it ONce found you can plkay with it, the parents, or children.

When you assign node location to a variable it becomes cached making it easier for the browser to find. Also known as storing a reference to the Object in the DOM tree.

## Handling Nodelists

- A NodeList is a collection of element nodes. Each node is given an index number. (much like arrays this starts at 0)
  - Nodelists has porperties and methods much like any other object
    - `length` property tells you how many items are in the NodeList
    - `item()` method returns a specific node from the item that you want (in the parenthesis).
      - However it's more common to use array syntax to retreive an item from a NodeList

MEthods beginning with `querySelector` will generate static lists as it only querys once, when the page is loaded. Using `getElementsBy...` return live NodeLists.

```JS
let hotItems = document.querySelectorAll('li.hot') //Stores the Nodelist in array format under the variable "hotItems"
if (hotItems.length > 0) { //If list of hot items contains something
  for (var i=0; i<hotIems.length; i++) { //looping through each item
    hotItems[i].className = 'cool'; //alter class attribute
  }
}
```

## DANGER AHEAD: WHITESPACE NODES

Traversing can be difficult as some browsers when they come across whitespace add a text node.

## ACCESS & UPDATE A TEXT NODE WITH NODEVALUE

When you select a TextNodeyou can retreive or ammed using `nodeValue` property.

in order to use this, you must be targeting a text node. If you do not know wether or not there will be element nodes alongside the text node, it's easier to work in the containing element.

`textContent` allows you to collect or update jus tthe text that is in the containing element (and it's children)
`document.getElementById('one').textContent;`

`innerHTML` When getting HTML from an element, will get the content including the markup

Editing the Domtree!

Adding! 

```JS
//Create a new element and store it in variable
let newLine = document.createElement('li');
//create a text node now and store it in a variable
let newItem - document.creatTextNode('apple')
//attach the new text node to the new element
newLine.appendChild(newItem);
//Find the position where new elelemtn should be created (Position [0] )
let position = document.getElementsbyTagName('ul')[0];
//Insert New element
position.appendChild(newLine); 
```
Removal!

```JS
//The element to remove targeting item #4 [3]
let removeLine = document.getElementsByTagName('li')[3];
// the containing element
let container = removeLine.parentNode;
// Finally Removing
container.removeChild(removeLine);
```

## CROSS SITE SCRIPTING (XXS) ATKS. 

If you add HTML to a page using innerHTML (or several other jQuerymethods) you need to be aware of XXS.

You can defend through several methods.

Validate input going to server

1. Only let visitors input the kind of characters they need when supplying information. This is called **validation**
/ Do not let untrusted users submit markup or JS.
2. Double check validation on server before displaying user content. This is important becasue users can bypass by turning JS off.
3. The database may safely contain markup and script from trusted sources, because it doesn't ever try to process code, it just stores it.
4.  As your data leaves the server all potentially dangerous characters should be escaped.
5. Make sure you are only inserting content generated by users into certain parts of template files.
6. Do not creat DOM fragments containing HTML from untrusted sources. 

Escaping user content

- HTML - escape these &<>`'"/ so they are displayed as characters and not processed as code.
- JS - Never include data from untrusted sources, it involves escaping all ASCII characters with a value oif less than 256 that are not alphanumeric.
- URLS - If you have links containing user input use the JavaScript `encodeURIComponent()` to encode the user input.

Adding user content

- JavaScript
  - DO: use textContext or innerText
  - DO NOT: use innerHTML

- JQUERY 
  - DO use: .text()
  - DO NOT: .html()

you can still use innerHTML ans .html() but make sure that

1. You controll ALL of the markup being generated. (Do not allow user to enter in markup)
2. The users content is escaped and added as text using the approaches noted above.

[0^]: Frequently directly quoted from[Better Programming:What’s the Difference Between Primitive Values and Object References in JavaScript?, by Chris Geelhoed](https://betterprogramming.pub/intermediate-javascript-whats-the-difference-between-primitive-values-and-object-references-e863d70677b)
