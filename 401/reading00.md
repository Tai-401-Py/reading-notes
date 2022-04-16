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


```