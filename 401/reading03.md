
# File input / output and exceptions

---

## [Read & Write in Py](https://realpython.com/read-write-files-python/)

A file consists of 3 major parts, the header, data, and end of file or (EOF)

File paths: 

When accessing a file you are using a string which is composed of 3 parts. 
1. Folderpath 
2. Filename
3. Extension (Prepnded by a . between it and the filename)

Line endings was standaradized for teleprinters and has it's roots back in the morse code days. 

When manipulating a file you should use a try-finally block so that the file will close no matter what once you're done with it. 

When reading a file, most commonly you wil use `.readline()` method to perform iteration over each line. 

When writing you can make use of the `.write()` and `.writelines()` methods

opening a file with the arg `a` wil lallow you to append when writing. 

The `__file__` attribute is a special attribute of modules, similar to `__name__`. It is: “the pathname of the file from which the module was loaded, if it was loaded from a file.”

### [Exceptions vs Syntax Errors](https://realpython.com/python-exceptions/)

Syntax - The parser has detected something wrong in a statement 

Exception - Syntax is correct but still has an error

`raise` this can be used to throw an exception, which can be used to moderate inputs

`assertion` assertionerror when an asserted statement returns false-y

`try` -> `except` can be used to handle errors, the try bing a normal part of the code, and the except being what runs if the try fails. 

`else` No exceptions, then run this code. 

There is also `finally` which will run regardless. 

NOTE: **Catching Exception hides all errors…even those which are completely unexpected. This is why you should avoid bare except clauses in your Python programs. Instead, you’ll want to refer to specific exception classes you want to catch and handle**

### Things I'd like to know more about 

IT really isn't clear from the docs exactly how to use `__enter__()` and `__exit__()` either that or I don't quite understand the terminology yet. Though it sounds interesting it feels way beyond my understanding at the moment and I feel like I'm going to need to revisit it. 