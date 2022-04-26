
# Python and understanding scope

---

## Scope 

### LEGB

Local, Enclosing, Global, Built-in 

These are the scope levels, not only that but this is also the order in  which python resolves when resolving names in a program.

In programming the scope of a name defines the area of a program in which you can unambiguously access that name. Most commonly you'll be using two types, local and global.

Since python is a dynamically typed language, variables come into existence whe nyou first assign them a value. 

import operations, assignments, function definitions, args in the context of functions, class definitions.  All of these create or in the case of assignment can update Python names.  

in python the concept of scope is closely realated to the concepts of namespace. They are stored in a special attribute called `__dict__` NAmes at the top level of a module are stored in the namepace. 

### Scopes

Local - Code block or body of any python fucntion or lambda expressions.  This contains anything that you defined inside a function. These names are only visible to the function. 

Enclosing - special scope for nested functions. if the local scope is an inner or nested function, then the enclosing scope  is the scope oif the outer function. The names in the enclosing scope are visible to the code from both inner and outer functions. 

Global - Top most scope - Everything can see this. 

Built in - this is a special scope that's loaded whenever you run a python program. This scope conatins all of the functions, exceptions and keywords that go into python. 


you can inspect the names and parameters  of a function using `.__code__`

```py
>>> square.__code__.co_varnames #variable names in scope
('base', 'result')
>>> square.__code__.co_argcount # How many arguments are in this scope
1
>>> square.__code__.co_consts # How many constants
(None, 2, 'The square of ', ' is: ')
>>> square.__code__.co_name # What is the name of the top level of this scope. 
'square'
```

To inspect names in your main gloal scope you can use `dir()` if you call it without any args then it will return of all names taht exist in your current global scope. 

- Try to avoid modifying global names as much as possible. 
    - they can be difficult to debug: almost any statement in the program can change a global variable
    - Hard to understand: You must be aware at all times of all teh statements that can access and modify global names. 
    - Impossible to reuse: The code is dependant on global names concrete to a specific program. 
 
 - Instead
    - Write self-contained **functions that rely on local names** rather than global ones.
    - Try to **use unique objects names**, no matter what scope you’re in.
    - **Avoid global name modifications** throughout your programs.
    -Avoid cross-module name modifications.
    - **Use global names as constants** that don’t change during your program’s execution.

### Things I would like to know more about

    - I would really like to boil down into the nuts and bolts of python and see how it uses it's own definitions to compile itself. Though that seems like a daunting task while I do stacked module learning. 