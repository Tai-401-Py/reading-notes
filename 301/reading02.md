
# React Component Life Cycle

---

## Reading questions

Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?

Render is what happens first

What is the very first thing to happen in the lifecycle of React?

Mounting is the first thing that happens

Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates

Constructor, render, componentDidMount, React Updates, componentWillUnmount
    
What does componentDidMount do?

componentDidMount is used to load anything using a network, or to initialize the DOM. You can also use setState(); but that can cause issues due to constant reRendering.

---

## Reading Notes

Components can be defined as classes or functions, they can be calles during the cycle of a componenet and allow you to update the current state of application and User Interface. 

Constructor for a ReactComponent is called before mounting, if it is a subclass you need to call super(props); to get access to the props, or they will return undefined

render(); is the only required method in a class component it examins this.props and this.state. this should not modify componenet state or can cause issues. 

componentDidMount(); this method is called immediately after a component gets mounted if you need to load a network request or initialize things do here. 


UNSAFE Lifecycle Events

UNSAFE_componentWillMount()
UNSAFE_componentWillUpdate()
UNSAFE_componentWillReceiveProps()

These events have lead to a lot of bugs and unintended side effects, so in React these are no longer in use without the UNSAFE tag.

---

## React State vs Props

What types of things can you pass in the props?

Anything that is passed from the parent and don't change inside a component. 

What is the big difference between props and state?

State is something inside a component and props are handled outside of the component and must be update outside.

When do we re-render our application?

When you change the state, you re-render

What are some examples of things that we could store in state?

Things that you need to store that requires re-rendering to display to the user. Typically this is based on what the user has done. If you have an input element it needs to be in state. 


---

## Things I want to know more about

How does one call to an API, also what is the definition of subscribe used in context of a react application. 

