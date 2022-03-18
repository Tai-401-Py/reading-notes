
# Thinking with React


What is the single responsibility principle and how does it apply to components?

Each component should do one job so that you can identify easily where the problem esists when something breaks. If it does more than one thing break it up into smaller components.

What does it mean to build a ‘static’ version of your application?

Build a version that has no interactivity, don't use state at all. Since state is reserved for interactivity. 

Once you have a static application, what do you need to add?

Intearctivity via state. Via minimal UI representation.

What are the three questions you can ask to determine if something is state?

passed via props? -> Does it remain unchanged -> Can you compute it based on any other state or props -> if all = false... It's not state.

How can you identify where state needs to live?

Identify every componenet that renders something -> Find a common component above all components that need the state, if you can't find one where it makes sense, make a component/  and attach it somewhere above the needed state. 

## Higher Order functions

What is a “higher-order function”?

Functions that operate other functions or create new functions. 

Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?

Line 2 is returning m if m is greater than n. 

Explain how either map or reduce operates, with regards to higher-order functions.

Map runs a function on all variables in an array creating an array with defined parameters, mapped to a new form. 

Reduce uns a function where it applies a single element of an array to the current element targeted by the reduce function, to build a value.  

## Things I want to know more about

I want to really know what I don't know, that I don't know. So that I can index things to learn about. There is so much in programming that I've barely tipped the surface. 