# Pythonisms


## Dunders

Dunder or doubleunder are unique methods, they let you emulate behaviours of built in types.

Object initialization `__init__`

Object representation: 
`__repr__`: The “official” string representation of an object. This is how you would make an object of the class. The goal of `__repr__ `is to be unambiguous.

`__str__`: The “informal” or nicely printable string representation of an object. This is for the enduser

Iteration: `__len__`, `__getitem__`, `__reversed__`

Callable Python Objects: `__call__`
You can make an object callable like a regular function by adding the `__call__` dunder method.


## [Iterators](https://dbader.org/blog/python-iterators)

Bare bones iterator protocol

    class Repeater:
        def __init__(self, value):
            self.value = value

        def __iter__(self):
            return RepeaterIterator(self)

    class RepeaterIterator:
    def __init__(self, source):
        self.source = source

    def __next__(self):
        return self.source.value   

the `__iter__` dundermethod is really a helperclass. 

RepeaterIterator looks like a straightforward Python class, but you might want to take note of the following two things:

In the `__init__` RepeaterIterator holds on to the “source” object that’s being iterated over.

In RepeaterIterator.__next__, we reach back into the “source” and return it

This causes an infinite loop. 

Here is something a bit healthierr

    class BoundedRepeater:
    def __init__(self, value, max_repeats):
        self.value = value
        self.max_repeats = max_repeats
        self.count = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.count >= self.max_repeats:
            raise StopIteration
        self.count += 1
        return self.value

This will go until the max number of repeats have been reached. 


## [Generators](https://dbader.org/blog/python-generators)

Generators hit a little differently, calling a generator function doesn’t even run the function. It merely creates and returns a generator object. the code only really runs if you call next on it. 

`yield` - this keyword suspends a function yet holds onto state. 