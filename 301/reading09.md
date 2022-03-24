# Reading 09

---

## [Functional Programming concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)


    What is functional programming?

Functional programming is a style of building out the archtechture and components of a computer program that prevents any change to state.

    What is a pure function and how do we know if something is a pure function?

If you pass it the same arguments it returns the same result and does not cause any observable side effects. 

    What are the benefits of a pure function?

They behave in a predictable way, are stable, consistent, and are easier to test

    What is immutability?

It is a state that can not be altered once it is created. If you want to change it, instead... Just create a new object.

    What is Referential transparency?

When a function is pure and has immutable data.

## [node.js Modules and require()](https://www.youtube.com/watch?v=xHLd36QoS4k)


    What is a module?

A Module is an independant set of code that is part of a larger code base

    What does the word ‘require’ do?
    
It allows something to be called on a global scale.
    
    How do we bring another module into the file the we are working in?
    
`let var = require('filename')` which will then go looking in that file for a module.exports. to be used
    
    What do we have to do to make a module available?

You would use `module.exports = function`

## Things I want to know more about

 Ireally would like to know more about other methods to call information from an API other than axios. 

 Do companies typically have thier own libraries, or leave the calling to you for which libraries to use when desgining something new.