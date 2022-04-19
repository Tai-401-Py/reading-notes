
# TESTS AND MODULES

---

## [In Tests we Trust](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)

Data abstracted from link above. 

**TDD** (test driven development) it's a startegy to think and write tests first

### Important aspects

- Naming conventions
    - Test name should always follow the concvention of the module. 
    - if named x.py then test should be named test_x.py
- Keep the tests seperate from the module code, but follow similar trees

- Structure (AAA)
    - Arrange - Organize data for input
    - Act - Test the code!
    - Assert - Was the code output what I was expecting 

- The cycle of TDD
    1. Write a test unit and make it fail.
    2. Write a feature and make the test pass
    3. Refactor the code - first time doesn't need to be beautiful. 

TDD helps code be more reliable as you can check after each change. 

### [What does the if __name__ == “__main__”: do?](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)

Material taken from GeeksforGeeks

Before executing code, the Python interpreter reads the source file and defines a few special variables. If the file is running as a source(main) program then it gets a special `__name__` assignment to be the value `__main__`

1. Every Python module has it’s __name__ defined and if this is ‘__main__’, it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.
2. If you import this script as a module in another script, the __name__ is set to the name of the script/module.
3. Python files can act as either reusable modules, or as standalone programs.
4. if __name__ == “main”: is used to execute some code only if the file was run directly, and not imported.

### What is recursion

Recursion requires a stack, or can be done iteravely. 

It continues to resolve itself until it reaches an end, and will continue repeating until an answer is given. This can be used to continue a login loop to prevent access or to compute numbers in a factorial. In each case the original method is weating for something to break it's loop by providing a value.  Most often it is something calling back to itself waiting for an answer on a stack to finally execute. 

### Things I'd like to know more about

Still can't quite wrap my head around the `__name__` `__main__` thing I really hope to find more guidance on that subject. 

Whiteboarding still seems like a strange concept and feels a lot more difficult to do on a computer than it would otherwise IRL. I would love to learn more about whiteboarding.