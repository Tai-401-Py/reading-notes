# Working with Strings

---

- Strings are the most common and simplest data structures.
  - Any text between a double or single quot is a string

In the middle of a string you can use some special characters to add more things.

`\n` Will Generate a new line

`\t` Will tab over 4 spaces

`\` Backslash can be used as an escape character.

---

### 3.1 Accessing Strings

Strings can be thought of as a sequence of characters, each character of the string has an individual index and can be accessed by it. `string[0]` will access the first character of a string. Using inverse such as `string[-1]` will acess the last char.

---

### 4.1 String Operations

The `in` operator can be used to check if a string is a part of another sring. This returns a boolean response. `if x in y:`

Strings can be added together (also called concatination)

`print('Spam' + 'egg')` -> 'Spameggs'

They can also be multiplied by integers repeating the string multiple times

`print('spam' * 3)`-> spamspamspam

---

### 5.1 String functions

Strings have many useful functions. 

They are accessed through `string.function()` where `function` is one of the following.

- `count(var)` returns how many times a vriable appears in a given string
- `upper` converts to uppercase
- `lower` converts to lowecase
- `replace(old,new)` replaces all instances of old with new

`len(string)` returns the length of the string (how many chars are in it)