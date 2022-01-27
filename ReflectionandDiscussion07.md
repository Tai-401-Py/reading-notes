
# Programming with Javascript

---

[Table of contents](README.md)

---

## Javascript Control Flow

---

**Control flow** is the order in which a computer executes statements in a script.

Ex. a script to validate a form submnitted

>`if (field==empty) {`

 `   promptUser();`

 `} else {`
 
 `    submitForm();`
>`}`

The above function would check to see if a form is completed with no empty fields and run a different function based on whether it's filled or not. 

## Functions in JS (JavaScript)

---

> // Declaring a function

`function var(*argument*){*logic*}`

or

let var = function(){*logic*}`

>//They are the same thing

A function is a block of code that is designed to performa particular task. It is executed when something invokes it. 

>`function var(x, y){`
`return x * y; // returns product of x and y`
>`}` 

**Syntax**

- Defined with `function` keyword, followed by **name** followed by **()**.
- **name** can contain letters,digits,underscores, and dollar signs. 
- **()** may contain parameter names seperated by commas
- code to be executed contained in **{}** after defining syntax.

**Invoking(Calling)**

- When an even occours (Click a button)
- When it is invoked (Called)
- Automatically (Self invoked)

**Function Return**

- When JS reaches a `return` statement, function will cease operating.
- If invoked from a statement JS will "return" to execute the code after invoking.
- Often computes **return value**. This value returns to caller

**Why Use Functions**

- allows you to reuse code many times.
- You can reuse code many times with different variables. 

**Refactoring**

Improving the internal structure of an existing program's source code, while preserving its external behavior. 

The noun “refactoring” refers to one particular behavior-preserving transformation, such as “Extract Method” or “Introduce Parameter".

**Arguments**

- Arguments are same as function input
- **()** contains variables called arguments seperated by `, `.

**LAB 07 Steps**

- Create function
  - `function var(){}`
- Decide what prompt to return to user
  - `let var = prompt(){}`
- Create Logic that changes response.
  - else/if/then logic
>`if(var) {`
>`response = 'output'}`
>`alert('response')`
- Check user input for valid input, if not valid resend to prompt

Don't forget to invoke function. 