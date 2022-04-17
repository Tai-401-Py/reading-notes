# Intro to Python

## Notes

### Variables

```py

# Variables are set with an = sign

this = that

# Variables can only be letters,numbers,underscores. They can not start with numbers. They will cause an error.

# Python is a case sensitive language so
# This = that and this = that are two different variables


```

Variables can be changed as many times as you want. Though make sure to try and not do this very often, it isn't good practice.

### Taking User input

To get user input you can use the input() function. It prompts the user for an input and returns what they enter as a string

```py
x = input()
print(x)

# By providing a string you can produce a prompt message. This will help clarify the request.

name = input("Enter your name: ")
print( 'Hello, ' + name)

```

### Working with input

Input only takes in a string, if you want it to return a number you can use the int() function `age = int(input())`

Alternatively you can return a number input as a string by using the str() function.

You can also convert to float using float()

Using input() multiple times to take in various inputs. When it executes the program flow stops until input is achieved by the user.

### In-Place and Walrus operators

In-place operators allow us to write code a bit more concisely `x = x = 3` can be written as `x += 3` this can also be done with -, +, /, % as well.

In-place operators can be used for any numerical operation (+, -, *, /, %, **, //).

They can also be used on strings

```py
x = spam
x += eggs
print(x) output:spameggs

x = a
x*=3
print(x) output:aaa
```

The walrus operator := allows you to assign variables a vlaue even if they don't exist yet.

```py
#you could write out an opeartion like this
num = int(input())
print(num)

# Or you can use the walrus operator and shorten it to 

print(num:=int(input()))
```

the walrus operator allows us to take in the new variable and set it with input at once.

### Booleans and Comparisons

Booleans come in two values True and False, valuse and variables can be compared using the == operator.

Another is the not equal comparison which is != which will also return a True or False value.

Comparison operators are also called Relational Operators.

You can also use  > or < operators for floats and integers, you can also compare them to each other. Greater than or equal >= or less than or equal <= can also be compared.

Lexicographically (the alphabetic order of words based on the alphabetical order of thier components) you can use less than or greater than to compare strings.

### if Statements

You can use if statements to run code if a certain condition holds/returns true. Otherwise they aren't carried out.

```py
# Python uses indentation to delimit blocks of code. Depending on logic indentation could be mandatory. Statements contained in the expression need indentation.
if expression:
  then do this
```

Note the colon at the end of the expression. This is needed to determine whjere the if statement terminates before checking boolean value.

If statements can aslo be nested one inside the other.

```py
num = 12
if num > 5:
  print("bigger than 5")
  if num <=47:
    print('it\'s between 5 and 47')
```

### Else Statements

Else statements run only if all other if statements prove false. Same with if staetments the sontaining code in the block should be indented.

```py
x = 4
if x == 5:
  print('yes')
  else:
    print('yo no')
```

In order to make multiple checks you can nest if else statements. Though only each if statement can only have one else statement.

A shorter way of using an else if statement is `elif`

### Boolean logic

It is used to make more complicated conditions for if statements that rely on more than one condition.

Boolean operators can take `and`, `or`, `not`

```py
print( 1 == 1 and 2 == 2)
True
print ( 1== 1 and 2 == 3)
False
# Note: Boolean operators can be used as many times as you want in an expression.
```

`or` statements will run if either are true.

### Multiple Operators & Conditions

Operator precidence `==` has a higher precedence than `or`

Python's order of operations is the same as that of normal mathematics: parentheses first, then exponentiation, then multiplication/division, and then addition/subtraction.

You can chain multiple conditional statements in an if statement using the boolean operators.

you can use multiple `and`, `or`, `not` operators to chain conditions.

### Lists

Lists are used to store items, they are created by using square brackets with commas separating items.

```py

words = ['hello', 'world', '!']

# They can be acessed through an index

print(words[0]) #hello

```

You can also create empty lists with `[]` just an empty set of brackets. some lists have a comma after the last item, it's not needed but perfectly valid.

Lists can also contain several different types of items.  Nesed lists can be used to represent 2d grids, such as matrices

Even stings have indexes they are condiered a list with each index representing a character, even spaces are considered characters.

Trying to access a non-existing index will produce an error.

### List Operations

The item at a certain index can be reassigned.

```py
nums = [7, 7, 7, 7, 7]
nums[2] = 5
print(nums) # [7,7,5,7,7]

# Lists can be added and multiplied in the same way as strings.

nums = [1, 2, 3]
print(nums + [4, 5, 6]) # [1, 2, 3, 4, 5, 6]
print(nums * 3) # [1,2,3,1,2,3,1,2,3]

```

To check if an item is in a list the `in` operator can be used. It returns True if the item occours one or more times in the list, and false if it doesn't. The `in` operator can also be used to determine wheter or not a string is a substring of another string.

you can also use the `not` operator to check if an item is not in a list.

### List functions

```py
#.append adds an item to the end of an existing list.

nums = [1,2,3]
nums.append(4)
print(nums) # [1,2,3,4]

#.insert allows you to add something to anywhere in a list

index = 2
nums.insert(index, 7)
print(nums) # [1,2,7,3] items after are shifted right

#.index method finds the first occourance and returns it's index

print(nums.index(2)) # [1] since the number 2 is at index 1

#.count(item) returns how many tiems a item occours in a list
#.remove(item) removes an item from a list
#.reverse() reverses and items in a list

```

To get the number of items in a luist you use the `len` function.

```py
nums=[1,2,3]
print(len(nums)) # 3 (That's how many items)
```

`max(list)` returns the list item with the highest value. `min()` dies the same for the smallest value.

### While loops

`break` will stop a while loop

`continue` statement will stop current itteration and proceed with the next one.

### for Loop

used to iterate over a given sequence, such as lists or strings.

```py
words = ['spam', 'egg', 'potato']
for word in words:
  print(word + '!') #['spam!', 'egg!', 'potato!']

```

### Range

`range()` function returns a sequence of numbers, by default it starts from 0, and increments by 1 and stops **before the specified number**

if we want to output the range as a list then we need to use the `list()` function

Range if called with one argument produces values from 0 to that argument, if given 2 arguments will produce values from the first to the seconda rgument.

A third argument will be called a step and `range()` will increment by it. You can also decrement with a -number.

### Code Reuse

DRY code (Don't Repeat Yourself), WET (Write Everything Twice). We like Dry code.

Any statement that consists of a word followed by information in parens is a function call. The words in front of the parens are function names, and the values in parent sepearated by commas are arguments

### Functions

You can creat your own functions using the `def` statement

you must define them vbefore they are called

### Arguments

Most functions take arguments and you can use multiple arguments in a function seperated by a comma `function(a,b,c)`

These arguments can also be used as variables.

### returniung from functions

Return statements can not be used outside of a function definition

They will also stop a function at the return.

### Comments

```py

# Will comment out code

def docstring()
"""
This is a Docstring and they are put below a functions first line to explain the function
"""

```

### Modules

Modules are peices of code that other people have written to fulfil common tasks such as generating random numbers.

```py

import module_name

# then use module_name.var() to acess it's functions

from module_name import sub_module

# this will allow you to import only a particular function from a module

from module_name import sub_module as new_name

# You can rename modules this is helpful if the module has a long or confusing name. 

```

### PY libraries

Many third-party Python modules are stored on the Python Package Index (PyPI).
The best way to install these is using a program called pip. This comes installed by default with modern distributions of Python. If you don't have it, it is easy to install online. Once you have it, installing libraries from PyPI is easy. Look up the name of the library you want to install, go to the command line (for Windows it will be the Command Prompt), and enter pip install library_name. Once you've done this, import the library and use it in your code.

Using pip is the standard way of installing libraries on most operating systems, but some libraries have prebuilt binaries for Windows. These are normal executable files that let you install libraries with a GUI the same way you would install other programs.

### Exceptions

Similar to try/catch in Javascript ||  Python has try/except

An except statement without any exceptions wil lcatch all errors (Use sparingly)

There is also finally, which will run code regardless.

You can raise exceptions using `raise` statement

### Assertions

An assertion is a sanity-check that you can turn on or turn off when you have finished testing the program.

An expression is tested, and if the result comes up false, an exception is raised.

Assertions are carried out through use of the assert statement.

```py
# The assert can take a second argument that is passed to the AssertionError raised if the assertion fails. 

assert (temp >=0), "colder than zero"

```

### Opening Files

```py
#py can be used to read and write file contents. Text files are easiset to manipulate
#you can use [r,w,a] read,write,append and then there is [b] which is binary mode which is used for audio and images
myfile = open("filename.txt", "r") #read access to filename.txt

#Be sure to close a file when you are done with it. 
myfile.close()

#.read can be used to read a file


```

### Sets

Sets can be combined using mathematical operations.

The union operator | combines two sets to form a new one containing items in either.

The intersection operator & gets items only in both.

The difference operator - gets items in the first set but not in the second.

The symmetric difference operator ^ gets items in either set, but not both.

Sets do not allow duplicate entries

### Data Structures

Python supports the following data structures: lists, dictionaries, tuples, sets.

When to use a dictionary:

- When you need a logical association between a key:value pair.
- When you need fast lookup for your data, based on a custom key.
- When your data is being constantly modified. Remember, dictionaries are mutable.

When to use the other types:

- Use lists if you have a collection of data that does not need random access. Try to choose lists when you need a simple, iterable collection that is modified frequently.
- Use a set if you need uniqueness for the elements.
- Use tuples when your data cannot change.

### itertools

The module itertools is a standard library that contains several functions that are useful in functional programming.
One type of function it produces is infinite iterators.
The function count counts up infinitely from a value.
The function cycle infinitely iterates through an iterable (for instance a list or string).
The function repeat repeats an object, either infinitely or a specific number of times.
Example:

```py
from itertool import count as cnt

for i in cnt(3):
  print(i)
```

  There are many functions in itertools that operate on iterables, in a similar way to map and filter.
Some examples:

takewhile - takes items from an iterable while a predicate function remains true;

chain - combines several iterables into one long one;

accumulate - returns a running total of values in an iterable.

There are also several combinatoric functions in itertool, such as product and permutation.
These are used when you want to accomplish a task with all possible combinations of some items.

### Classes

We have previously looked at two paradigms of programming - imperative (using statements, loops, and functions as subroutines), and functional (using pure functions, higher-order functions, and recursion).

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

### Magic Methods

Magic methods are special methods which have double underscores at the beginning and end of their names.

They are also known as **dunders**.

So far, the only one we have encountered is `__init__`, but there are several others.

They are used to create functionality that can't be represented as a normal method.

One common use of them is operator overloading.

This means defining operators for custom classes that allow operators such as + and * to be used on them.

An example magic method is `__add__` for +.

List of magic methods for common operators

- `__sub__` for -
- `__mul__` for *
- `__truediv__` for /
- `__floordiv__` for //
- `__mod__` for %
- `__pow__` for **
- `__and__` for &
- `__xor__` for ^
- `__or__` for |

Python also provides magic methods for comparisons.

- `__lt__` for <
- `__le__` for <=
- `__eq__` for ==
- `__ne__` for !=
- `__gt__` for >
- `__ge__` for >=

There are several magic methods for making classes act like containers.

- `_len__` for len()
- `__getitem__` for indexing
- `__setitem__` for assigning to indexed values
- `__delitem__` for deleting indexed values
- `__iter__` for iteration over objects (e.g., in for loops)
- `__contains__` for in

There are many other magic methods such as `__call__` for calling objects as functions, and `__int__`, `__str__`, and the like, for converting objects to built-in types.

### Object Lifecycle

The lifecycle of an object is made up of its creation, manipulation, and destruction.

The first stage of the life-cycle of an object is the definition of the class to which it belongs.

The next stage is the instantiation of an instance, when `__init__` is called. Memory is allocated to store the instance. Just before this occurs, the `__new__` method of the class is called. This is usually overridden only in special cases.

After this has happened, the object is ready to be used.

When an object is destroyed, the memory allocated to it is freed up, and can be used for other purposes.

Destruction of an object occurs when its reference count reaches zero. Reference count is the number of variables and other elements that refer to an object.

If nothing is referring to it (it has a reference count of zero) nothing can interact with it, so it can be safely deleted.

In some situations, two (or more) objects can be referred to by each other only, and therefore can be deleted as well.

The del statement reduces the reference count of an object by one, and this often leads to its deletion.

The magic method for the del statement is `__del__`.

The process of deleting objects when they are no longer needed is called garbage collection.

In summary, an object's reference count increases when it is assigned a new name or placed in a container (list, tuple, or dictionary). The object's reference count decreases when it's deleted with del, its reference is reassigned, or its reference goes out of scope. When an object's reference count reaches zero, Python automatically deletes it.

```py
a = 42  # Create object <42>

b = a  # Increase ref. count  of <42> 

c = [a]  # Increase ref. count  of <42> 



del a  # Decrease ref. count  of <42>

b = 100  # Decrease ref. count  of <42> 

c[0] = -1  # Decrease ref. count  of <42>

```

NOTE: Lower level languages like C don't have this kind of automatic memory management.

### Data Hiding

A key part of object-oriented programming is encapsulation, which involves packaging of related variables and functions into a single easy-to-use object - an instance of a class.

A related concept is data hiding, which states that implementation details of a class should be hidden, and a clean standard interface be presented for those who want to use the class.

In other programming languages, this is usually done with private methods and attributes, which block external access to certain methods and attributes in a class.

The Python philosophy is slightly different. It is often stated as "we are all consenting adults here", meaning that you shouldn't put arbitrary restrictions on accessing parts of a class. Hence there are no ways of enforcing a method or attribute be strictly private.

**However, there are ways to discourage people from accessing parts of a class, such as by denoting that it is an implementation detail, and should be used at their own risk.**

**Weakly private methods** and attributes have a **single underscore** at the beginning.

This signals that they are private, and shouldn't be used by external code. However, it is mostly only a convention, and does not stop external code from accessing them.

Its only actual effect is that from module_name import * won't import variables that start with a single underscore.

**Strongly private methods** and attributes have a **double underscore** at the beginning of their names. This causes their names to be mangled, which means that they can't be accessed from outside the class.

The purpose of this isn't to ensure that they are kept private, but to avoid bugs if there are subclasses that have methods or attributes with the same names. 

NOTE: you can still call strongly private methods by calling weakly private methods `_b__a`

### Class Methods


Methods of objects we've looked at so far are called by an instance of a class, which is then passed to the self parameter of the method.

Class methods are different - they are called by a class, which is passed to the cls parameter of the method.

A common use of these are factory methods, which instantiate an instance of a class, using different parameters than those usually passed to the class constructor.

Class methods are marked with a classmethod decorator. `@classmethod`

Static methods are similar to class methods, except they don't receive any additional arguments; they are identical to normal functions that belong to a class.

They are marked with the staticmethod decorator. `@staticmethod`

### Properties

Properties provide a way of customizing access to instance attributes.

They are created by putting the property decorator above a method, which means when the instance attribute with the same name as the method is accessed, the method will be called instead.

One common use of a property is to make an attribute read-only. `@property`

Properties can also be set by defining setter/getter functions.

The setter function sets the corresponding property's value.

The getter gets the value.

To define a setter, you need to use a decorator of the same name as the property, followed by a dot and the setter keyword.

The same applies to defining getter functions. 

```py

@property
  def bork_maybe(self, boolean)

@bork_maybe.setter
  def bork_yes():


```

### Python Regex

Regular expressions in Python can be accessed using the re module, which is part of the standard library.

After you've defined a regular expression, the re.match function can be used to determine whether it matches at the beginning of a string.

If it does, match returns an object representing the match, if not, it returns None.

To avoid any confusion while working with regular expressions, we would use raw strings as r"expression".

Raw strings don't escape anything, which makes use of regular expressions easier. 

```py
import re

pattern = r"spam"

if re.match(pattern, "spam"):
  print("match get")
else:
  print('nope')

```

Other functions to match patterns are `re.search` and `re.findall`.

The function `re.search` finds a match of a pattern anywhere in the string.

The function `re.findall` returns a list of all substrings that match a pattern. 

The function `re.finditer` does the same thing as `re.findall`, except it returns an iterator, rather than a list. 

The regex search returns an object with several methods that give details about it.

These methods include `.group` which returns the string matched, `.start` and `.end` which return the start and ending positions of the first match, and `.span` which returns the start and end positions of the first match as a tuple.

One of the most important re methods that use regular expressions is sub.

Syntax: `re.sub(pattern, repl, string, count=0)`