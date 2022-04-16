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
```