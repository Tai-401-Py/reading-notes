
# Welcome to 401

---

## Pain and Suffering

The difference between pain and suffering

Pain is what allows for growth, suffering is without purpose. The greater the growth the greater the pain. Remember that your pain is only temporary while you're growing. They are Growing Pains. 

Over the next 10 weeks, consider your pain and what it means to you. The story you tell yourself with the pain you experience. 

|ASK|WHAT IT MEANS|
---|---|
|What’s your perspective?| Look at the pain you experience from a positive standppoint| 
|Why are you doing this?| Keep in mind your goals as you struggle, they will get you through|
|Do you want what comes at the end of this journey?| The Journey is half the battle, keep on fighting|
|Are you doing this for you?|Don't be here for someone else, you are here because you want to be here|

---

## Big O Notaion

Notes taken from [Big O Notation](https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation) by Rob Bell

- O(1) - Describes algorithms that will always exeute regardless of size and data set in the same time. 
- O(n) - Algorithm that has a linear growth in performance. Notation always assumes upper limit for execution.
- O(n^2) - Algorithm that has performance that is square to the size of the data set, most commonly in things that have nested iterations over data sets. 
- O(2^n) - Algorithms that the growth will double with each itteration of the input data set. ex. fibbonacci sequence
- O(log N) - Algorithms that grow quickly then flatten out, most commonly data reading and writing. 

When working with data sets, consider, what is most applicable in big O notation. 


## Facts and Myths about Python Names and Values

Info taken from PyCon2015 [Lecture by Ned Batchelder](https://www.youtube.com/watch?v=_AEJHKGk9ns)

Python is simple, it works very siumilar to other laguages till it doesnt... 

Names refer to values - Assignment makes the name refer to the value. Regardless of how they are assigned 

Names are reassigned independantly

Values live in memory until there are no references. Once all names are gone, the value is too. 

Assignment never copies data - There is only ever one list no matter how many things reference it or which variable you change until you reassign the name to a different value.

Immutable types are: ints, floats, strings, tuples -> They can not Alias

When you change an immutable value you actually rebind it. Changing a mutable value mutates it. Though you can still rebind mutable values.

Since things are only kept in memory while you have something reference it, it is impornatn to track keys and values because once there are no more keys to the value, the value disappears. When returning be sure to return as a name so that your variable can be kept in memory while it is being reassigned

Wenever possible avoid mutating lists and instead make a new list. 

Any name can refer to any value. 

Names have no type -> Values have no scope. 

[python tutor](https://pythontutor.com/) this will visualize your code so you can track your variables. 

Never mutate a default value for an arg because you could theoretically cause it to grow exponentially and it will in turn surprise you. 