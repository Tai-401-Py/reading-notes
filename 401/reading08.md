
# [List comprehensions in python](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)

## Syntax

There are three ingredients neccesary for list comprehension to work.

`variable = [Expression for Object in List]`

1. The Expression - Nested in square brackets
2.Object - the item inside square brackets
3.List - The iterable list of objects to build our new list from. 

List comprehensions are an elegant way to manage and create lists.

In Python they can be a much more compact way to create/populate lists

They are way more flexible than for loops and is usually faster than other methods. 

### Creating lists using loops and list comprehension.

You can use math calculations to populate number lists quite easily using the range function. 

You can aslo apply expressions to established lists 

`numbah = [2, 3, 7, 5]`
`multiply_it = [ x*3 for x in numbah]`

You can also apply filters to exclude certain items from list by applying if statements to the end of the whole expression. 

This can also be used to target strings as strings are really just lists where each character is an index. 

you can also use `.lower` and `.upper` to modify whole strings of characters.

using `isdigit()` you can extract just numbers from a sting. 

Thorugh creating  our own functions we can also apply them dunring list comprehension. 

Through these methods you can make more compact calculations. 