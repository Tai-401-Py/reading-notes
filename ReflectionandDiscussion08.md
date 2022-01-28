
# Reflection and Discussion 08

---

## Loops and Operators

### Operators

JS has both binary (multiple operand) and unary (one operand) operators.

|Operand1|operator|operand2|
---|---|---|


Typically

Types of operators

- Assignment operator
- Comparison operator
  - != : inequality operator
  - !== : strict not equal
  - == : equal
  - === : strict equal
- Arithmentic operator
  - ++ : Increment adds one to operand
  - `--` : Decrement subtracts one from operand
- Bitwise logical operators
  - probably not going to use for the time being
    - worry later
- Logical operators
  - `&&` - Logical and - Check op1 if true check op2
  - `||` - Logical or - return op1 if true else return op2
  - `!` - Logical NOT - Returns false if its single operand that can be converted to true; otherwise, returns true
- delete operator
  - `delete` deletes  objects property
    - `delete object.property;`
    - `delete object[propertyKey];`
    - `delete objectName[index];`


## Computer Logic


## Computer Loops

One of the main building blocks of code. 

`while` while function runs while  statement is true and continues till it's false.

A for loop 

- we set iteration count

`for( i=0; i > 10; i++){}`
|'i=0'|'i>10'|'i++'|
|---|---|---|
|initialization|condition|update|
|initial expression|condition expression|increment expression|

Avoid infinite loops, conditions must always eventually become false.

**Label** provides a statement identifier that lets you refer to it later, you can use the label to id the loop and use it to break or continue loop.
