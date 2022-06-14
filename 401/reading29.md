# ES6 Overview

## [ES6 Syntax and Feature Overview](https://www.taniarascia.com/es6-syntax-and-feature-overview/)

Variable Declarations

|Keyword|Scope|Hoisting|Can be Reassigned|Can be Redeclared|
---|---|---|---|---|
|var|function scope|yes|yes|yes| 
|let|block scope|no|yes|no|
|const|block scope|no|no|no|



- Arrow functions: a shorter way of creating a function expression. 

- Concatenation/string interpolation: Expressions can be embedded in template literal strings.

- Multi-line strings: Using template literal syntax, astring can span multiple lines without the need for concatenation.

- Implicit returns: The return keyword is implied and can be omitted if using arrow functions without a block body.

- Method def shorthand: Function keyword can be omitted when assigning methods on an object.

- Default parameters: Functions can be instantiated default parameters, which will be used only if an argument is not invoked.

## React

Converting a Function to a Class

- Create a class with the same name, that extends React.Component.
- Add a single empty method to it called `render()`.
- Move the body of the function into the `render()` method.
- Replace `props` with `this.props` in the `render()` body.


Create an ES6 class (Links to an external site.), with the same name, that extends React.Component.
Add a single empty method to it called render().
Move the body of the function into the render() method.
Replace props with this.props in the render() body.
Delete the remaining empty function declaration.
Adding Local State to a Class
We will move the date from props to state in three steps:


## [Tailwind CSS](https://tailwindcss.com/docs/utility-first)

Traditionally, CSS is used to style web pages

With Tailwind, you style elements by applying pre-defined classes directly in your HTML.

```js
<div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center space-x-4"> 
	<div class="shrink-0"> 
		<img class="h-12 w-12" src="/img/logo.svg" alt="ChitChat Logo"> 
	</div> 
	<div> 
		<div class="text-xl font-medium text-black">ChitChat</div> 
		<p class="text-slate-500">You have a new message!</p> 
	</div> 
</div>
```

Looking at some of the classes used and the stylings associated

- Tailwind’s flexbox and padding utilities (flex, shrink-0, and p-6) to control the overall card layout
- The max-width and margin utilities (max-w-sm and mx-auto) to constrain the card width and center it horizontally
- The background color, border radius, and box-shadow utilities (bg-white, rounded-xl, and shadow-lg) to style the card’s appearance
- The width and height utilities (w-12 and h-12) to size the logo image
- The space-between utilities (space-x-4) to handle the spacing between the logo and the text
- The font size, text color, and font-weight utilities (text-xl, text-black, font-medium, etc.) to style the card text


