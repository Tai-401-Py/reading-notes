
# Classes, Objects, Recursion

---

## [Classes and Objects](https://www.learnpython.org/en/Classes_and_Objects)

Objects are the encapsulation of variables and functions put into a single entity. Objects get their varibles from classes which are templates to create objects. 

### Objects and Classes

Another very popular paradigm is object-oriented programming (OOP).
Objects are created using classes, which are actually the focal point of OOP.
The class describes what the object will be, but is separate from the object itself. In other words, a class can be described as an object's blueprint, description, or definition.
You can use the same class as a blueprint for creating multiple different objects.

Classes are created using the keyword class and an indented block, which contains class methods (which are functions).

The `__init__` method is the most important method in a class.
This is called when an instance (object) of the class is created, using the class name as a function.

All methods must have self as their first parameter, although it isn't explicitly passed, Python adds the self argument to the list for you; you do not need to include it when you call the methods. Within a method definition, self refers to the instance calling the method.

Instances of a class have attributes, which are pieces of data associated with them.

```py
class Dog:
  def __init__(self, color, name)
    self.color = color
    self.name = name


#Classes can have other methods defined to add functionality to them.
#Remember, that all methods must have self as their first parameter.
#These methods are accessed using the same dot syntax as attributes.
#Example:
  def bork(self):
    print("bork bork!")

baxter = Dog('White', 'baxter')
baxter.bork()

```

Classes can also have class attributes, created by assigning variables within the body of the class. These can be accessed either from instances of the class, or the class itself.

### Class Inheritance

Inheritance provides a way to share functionality between classes.

Imagine several classes, Cat, Dog, Rabbit and so on. Although they may differ in some ways (only Dog might have the method bark), they are likely to be similar in others (all having the attributes color and name).

This similarity can be expressed by making them all inherit from a superclass Animal, which contains the shared functionality.

To inherit a class from another class, put the superclass name in parentheses after the class name.

```py
#in this instance Animal is the superclass of dog

class Dog(Animal):

# Inheritance can be indirect, in this case puppy inherits dog which also inherits animal, so puppoy inherits animal as well. 
class Puppy(Dog):
```

The function `super` is a useful inheritance-related function that refers to the parent class. It can be used to find the method with a certain name in an object's superclass.

```py
class Puppy(Dog):
  super().bork()

```

### [Thinking Recursively](https://realpython.com/python-thinking-recursively/)

Recursive algorithms typically represent a case and attempt to solve it, and if it can't it uses the same equation to subdivide the problem until solved, or to infinity. 

Behind the scene recursive functions create a stack call, then begins to resolve as they reach an end case, and the prior case returns a result. 

You can maintain state by keeping it in a global scope then call it with the `global` call. Though it is much preferred to thread the state through each recursive call. 

Sadly python doesn't support tail-call elimination, if you exceed call stack depth it will cause a stack overflow. **Typical recursive limit is 3000**

### [Python Testing and Coverage](https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage)

When writing a test case it can be easy to cover only the positive cases, but you can'[t forget to cover every aspect of your code. If you're throwing exceptions you should test the exceptions to make sure those are throwing properly as well. This way your scope of coverage for testing is 100%. 

### Things I Would Like To Know More About

Potentially using classes as a way to script characters in a videogame as a way to store stats and leveling statistics  in order to really flesh out a character behind the scenes to see how that would work. 