# Class 10 REading Notes

## Debugging code

### Execution context

- Global
  - Variables detailed outside of function
- Function
  - Typically self contained in a function and unable to be called outside of.

Nested functions can call variables from functions they are nested in, but can not call to variables that are nested deeper in another function iside them. 

### Error objects 

- Synatx : You're missing something that follows the rules of the code language ( typically a missed character or typo)
- Reference Error - Typically a missing variable, or an undefined function.
- URI Error - Characters not escaped.
- Type Error 
  - Incorect Casing
  - Method doesn't exist (function doesn't exist)
  - Dom Node Doesn't Exist
- Range Error
  - Number outside of range
  - Doesn't follow numbering rules set
- NaN - It's not a number, get a number.

### Handling Errors

DEV CONSOLES in browser. 
Error handling code. 
console.log()!!!!!
console.table()!!

Stepping through code line by line to handle everything. To watch how it handles rather than running as fast as possible. 

Create conditional breakpoints. 

Try->Catch->Finally
Try -> Run First
Catch -> If doesn't run, do this,
Finally -> Still run this regardless of try and catch. 