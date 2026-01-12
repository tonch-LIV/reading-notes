# 102_Read_07

- [Control Flow](#control-flow)
- [Functions](#functions)
  - [W3 Schools](#w3-schools)
    - [Structure](#structure)
    - [Invocation](#invocation)
    - [Arrow Functions](#arrow-functions)
    - [Local Variables](#local-variables)
    - [Parameters vs Arguments](#parameters-vs-arguments)
    - [Functions as Variables](#functions-as-variables)
  - [MDN](#mdn)
- [Operators](#operators)
  - [Assignment](#assignment)
  - [Arithmetic](#arithmetic)
  - [Comparison](#comparison)
  - [Logical operators](#logical-operators)
- [Expressions and Operators](#expressions-and-operators)
  - [Bitwise](#bitwise)
- [Answers](#answers)

## Control Flow

Refers to the order in which the computer executes statements in a script. Traditionally, code is run top to bottom, line after line. The exception would be structures such as, conditionals (if/else) and loops, which change the control flow.  
JavaScript is well known to include many control structures like conditionals, loops, and functions. Control flow means reading the script, but also taking into consideration the order of execution.  

## Functions

### W3 Schools

Functions are fundamental program building blocks, that are often reusable, and are executed when "called/invoked" to perform a particular task.  

``` js
function pair(a, b) {
 return a * b;
}
```

would return whatever numbers would be substituted for "a" and "b" when calling the functions. For example, `function pair(7, 3)` would return `21`.  

#### Structure

`function` is the keyword that defines all functions. The structure is as follows `function functionName() {}`. naming rules for functions are the same as for variables[link]. optional parameters go inside `()` and the code to be executed would go between `{}`.  
Since functions allow for reusable blocks of code, they allow for better organization and ultimately, efficiency in creating and executing code.

#### Invocation

The code within the function `{}` executes, when it is called/invoked through the use of the `()` operator.

```js
// convert miles to kilometers
function toMiles(km) {
 return km * (.62);
}
// class the function
let distance = toMiles(5);
```

would output 5km as `3.1` miles. We are replacing `(km)` with the value of `5`, it is being multiplied against `(.62)`, and the result is beig returned to the user.  

If you were to invoke a function with incorrect parameters; missing value(s) within `()`, it can lead to incorrect answers. Similarly, if you were to invoke the function without `()` after the function, you'd get the function itself as the output.  
`toMiles` is the function object; the function itself. `toMiles()` is what leads to the output of the function.  

#### Arrow Functions

Introduced in later revicions of ES6[link], arrows `=>` allow for the use of shorter function syntax.

#### Local Variables

Variables declared within the function; cannot be accessed from outside the function. Potentially, allows for using the same name for functions in different functions that produce different results.  
Local variables are created and deleted only during the life of the function; do not exist outside of function.

#### Parameters vs Arguments

Parameters are the names listed in the function definition, while arguments are the values received be the function. Values, you input to replace the placeholder (parameters) when calling the function.

#### Functions as Variables

In all types of formulas, assignments, and calculations; functions can be used as variables. Reduces the amount of lines written.  
Instead of,

```js
let a = toMiles(5);
let distance = "The library is " + a + " miles away.";
```

We use,

```js
let distance = "the library is " + toMiles(5) + " miles away.";
```

### MDN

## Operators

Operators are used for arithmetic and logical computations (`=`, `+`, etc.). They are used to hold expressions together.

### Assignment

- `=`, known as the Assignment operator, assigns value.  
`let x = 10` means everytime `x` is invoked, it will be replaced by `5`.

Other assignment operators include,

|Operator |Example   |Same As         |
|---------|----------|----------------|
|=        |x = y     |x = y           |
|+=       |x += y    |x = x + y       |
|-=       |x -= y    |x = x - y       |
|*=       |x *= y    |x = x * y       |
|/=       |x /= y    |x = x / y       |
|%=       |x %= y    |x = x % y       |
|**=      |x **= y   |x = x ** y      |
|<<=      |x <<= f() |x = x << f()    |
|>>=      |x >>= f() |x = x >> f()    |
|>>>=     |x >>> f() |x = x >>> f()   |
|&=       |x &= f()  |x = x & f()     |
|^=       |x ^= f()  |x = x ^ f()     |
|\|=      |x \|= f() |x = x \| f()    |
|&&=      |x &&= f() |x && (x = f())  |
|
|

### Arithmetic

- `+`, known as the Addition (Concatenation, for strings) operator, adds values.  
`let x = 10, y = 5, z = x + y;` will return `15` whenever `z` is invoked.  

Can also be used to add strings together (`+` or `+=`) or strings to numbers.  
If you add strings and numbers, the number results in being part of a string.

- `*`, known as the Multiplication operator, multiplies values.  
`let x = 10, y = 5, z = x * y;` will return `50` for `y`.  

A few more mathematical operators,

|Operator|Description                  |
|--------|-----------------------------|
|+       |Addition (Unary)             |
|-       |Subtraction (Unary)          |
|*       |Multiplication               |
|**      |Exponentiation               |
|/       |Division                     |
|%       |Modulus (Division Remainder) |
|++      |Increment (Unary)            |
|--      |Decrement (Unary)            |

### Comparison

- `>`/`<`, known as the Comparison operator(s), compares values.  
`let x = 10, y = 5, z = x > y;` will return `true` in this case, or `false` should the answer warrant.  

Operands used in this sense can be numerical, strings, logical, or object values. If the operands are not of the same type, an attempt will be made to convert them to a fitting type for conversion, usually numerically. Exceptions being `===` and `!==` which resolve to strict equality and inequality.

Additional comparison operators are,

|Operator |Description                       |Example  |
|---------|----------------------------------|---------|
|==       |equal to                          | x == 5  |
|===      |equal value and equal type        | x === 5 |
|!=       |not equal                         | x != 5  |
|!==      |not equal value or not equal type | x !== 5 |
|>        |greater than                      | x > 5   |
|<        |less than                         | x < 5   |
|>=       |greater than or equal to          | x >= 5  |
|<=       |less than or equal to             | x <= 5  |

**note: `=>` is the notation used for [Arrow functions](#arrow-functions)*

### Logical operators

|Operator |Description         |
|---------|--------------------|
|  &&     |logical AND         |
|  \| \|  |logical OR          |
|  !      |logical NOT (Unary) |
|  ??=    |Nullish coalescing  |

## Expressions and Operators

There are two types of expressions.  

- Ones with side effects (like assigning values, `x = 10`).
- Evaluative ones (`5 + 10` would resolve by doing the calculation and returning 15, rather than returning `5 = 10`).  

An expression is a unit or block of code that points/leads to a assigned value. Operators are subject to presedence (order of operations; PEMDAS, etc.). Grouped expressions with the use of `()` can override the precedence of operators over others, such as in arithmetic operations.  

### Bitwise

Treats decimal (0-9), hexadecimal (0-15), and octal (0-7) operand values as if they were a set of 32 bits (000 000 00 x4).  
If the value has more the 32 bits, their most significant bits (leftmost) will be discarded. The operands in the expression will be "compared" by their bit values, bit by bit.

## Answers

1. What is control flow?
    - Control flow regards to the order in which code is executed once run.
2. What is a JavaScript function?
    - Blocks of code which you can reuse by calling/invoking them and have them output different results based on the parameters given.
3. What does it mean to invoke - or call - a function?
    - Invoking/calling refers to the act of recalling the function in different places throughout the script/code.
4. What are the parenthesis () for when you define a function?
    - The parenthesis are the optional parameters operator. you can list placeholder values within them when you define the function.
