
# Reading 04

## React Docs - Forms

---

What is a ‘Controlled Component’?
    An input form whose element is value is controlled by React.
Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
    There are benefits to both, waiting to store user response uses less overall resources as you do not need to re-render anything, however updating as you type is much more responsive
How do we target what the user is entering if we have an event handler on an input field?
    we use a state to save the input, for use as a prop elsewhere.

Why would we use a ternary operator?

I's an easier way to write an if else statement to execute other code blocks.

Rewrite the following statement using a ternary statement:

```js
if(x===y){
  console.log(true);
} else {
  console.log(false);
}

x === y ? console.log(true) : console.log(false)
```

Note: you can also nest ternary statement

` if ? is true ? else if : is false`


## things I want to know more about

I've taken a look ahead and I'm really interested in active sorting. 

I wonder if you can get things to load in one at a time with a delay to look like cards being dealt.