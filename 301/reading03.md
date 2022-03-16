# Passing Functions as Props

## Lists and Keys

    What does .map() return?
      It returns an array
    If I want to loop through an array and display each value in JSX, how do I do that in React?
      You would map the array and assign it to a var and use that var in {} brackets. 
    Each list item needs a unique ____.
      key
    What is the purpose of a key?
      It helps react identify which items have changed, are added, or removed


What is the spread operator?
List 4 things that the spread operator can do.

- Spreads an array into seperate arguments
- Adding to a state in react
- Combining Objects
- Concatenating or combining arrays

Give an example of using the spread operator to combine two arrays.
`const array = [...arr1,...arr2]`

Give an example of using the spread operator to add a new item to an array.
`const array = ['item', 'item', ...arrItem]`

Give an example of using the spread operator to combine two objects into one.

`const objCombine = {...objOne,...objTwo,...objThree}`

## How to pass Functions Between components

In the video, what is the first step that the developer does to pass functions between components?
  Create the function wherever the state is going to change

In your own words, what does the increment function do?

increment function is just a name, it wouyld do the same regardless of name of function. Specifically it matches the name then increments the count of that object in which the name matches.

How can you pass a method from a parent component into a child component?

this.prop

How does the child component invoke a method that was passed to it from a parent component?

you pass a function through to the child through props. then create a function you call to which acesses the props function

## Things I want to know more about

How to use the spreader operatot to convert NOdeList and Arguments into arrays and how to then access their functionality.

What else can Bootstrap really do? I don't think I've really tapped evena  fraction of functionality.
