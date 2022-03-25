
# In memory storage

[Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)

    What is a ‘call’?

A request/invocation 

    How many ‘calls’ can happen at once?

Only one at a time, sorry no multi-threading here

    What does LIFO mean?

Last In, First Out

    Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.

```js
`funone(){};                    funthree()
funtwo(){funone()};             funtwo()
funthree(){funtwo()}            funone()
```

These will execute from 3->2->1> due to FILO

    What causes a Stack Overflow?

Recursive fucntions that call themselves woithout end and create loops. 


[JavaScript error messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)



    What is a ‘refrence error’?

Trying to use something that doesn't exist

    What is a ‘syntax error’?
    
Cannot be parsed, function can not be executed because parameters are wrong

    What is a ‘range error’?
    
Give an invalid value for something

    What is a ‘tyep error’?
    
variable is of a type it's not expecting

    What is a breakpoint?
    
Breakpoint is a point in the program which the code will stop executing. 

    What does the word ‘debugger’ do in your code?

IT allows you to see the history of thigns that ran.

## Things I want to know more about

Did I mention that I am frustrated about not getting a carousel to work in a modal....