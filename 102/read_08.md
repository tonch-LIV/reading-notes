# 102_Read_08

- [Expressions and Operators](#expressions-and-operators)
  - [Comparison](#comparison)
  - [Assignment](#assignment)
- [Loops](#loops)
  - [for statements](#for-statements)
  - [while statements](#while-statements)
- [Answers](#answers)

## Expressions and Operators

A value that is represented by a valid unit of code. When the unit is utilized, it will resolve to the value to which it was assigned to. Evaluative and Assignment expressions are the two types of expressions.

### Assignment

Uses the (=) sign (assignment operator) to assign a value to the left operand (the value(s) on the left side of the operator), to the right operand. Compound assignment operators listed in the table below, add to the functionality of the assignment operator.

| Name                             | Shorthand      |Meaning              |
|----------------------------------|----------------|---------------------|
| Assignment                       | `x = f()`      |  `x = f()`          |
| Addition assignment              | `x += f()`     |  `x = x + f()`      |
| Subtraction assignment           | `x -= f()`     |  `x = x - f()`      |
| Multiplication assignment        | `x *= f()`     |  `x = x * f()`      |
| Division assignment              | `x /= f()`     |  `x = x / f()`      |
| Remainder assignment             | `x %= f()`     |  `x = x % f()`      |
| Exponentiation assignment        | `x **= f()`    |  `x = x ** f()`     |
| Left shift assignment            | `x <<= f()`    |  `x = x << f()`     |
| Right shift assignment           | `x >>= f()`    |  `x = x >> f()`     |
| Unsigned right shift assignment  | `x >>>= f()`   |  `x = x >>> f()`    |
| Bitwise AND assignment           | `x &= f()`     |  `x = x & f()`      |
| Bitwise XOR assignment           | `x ^= f()`     |  `x = x ^ f()`      |
| Bitwise OR assignment            | `x \|= f()`    |  `x = x \| f()`     |
| Logical AND assignment           | `x &&= f()`    |  `x && (x = f())`   |
| Logical OR assignment            | `x \|\| = f()` |  `x \|\| (x = f())` |
| Nullish coalescing               | `x ??= f()`    |  `x ?? (x = f())`   |

#### Assigning to properties

In relation to objects, the left side of the assignment expression can make assignments to properties of that expression. Not possible if expression does not evaluate to object.

#### Destructuring

Syntax that allows one to [pull](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring) specific data from within an array or object, through the use of syntax that follows the layout of array/object literals. Less statements needed to be made to extract more than one set of values.

#### Evaluation and nesting

Nesting and chaining is often [discouraged](https://github.com/airbnb/javascript/blob/master/README.md#variables--no-chain-assignment) by some, due to expressions leading to surprising behavior. They are still used and can appear in modern day code, so it is vital to learn and understand them. Results from expressions themselves can in turn be assigned to other vaariables, logged, put insided array/object, functions, etc. Putting a variable chain in `const`, `let`, or `var` will sometimes not work, leading to unexpected results if only the leftmost variable is declared.

### Comparison

Compares the operands on both sides ofthe operator and returns a logical vlaue depending wether the statement/comparison is true. Operands can be either numbers, strings, logical, or object values. If the two operands are of different value types, an attempt will be made to convert them to an appropriate type for comparison, usually numerically. `===` and `!==` being strict equality/inequality operators are the exception of the conversion rule for obvious reasons.

| Operator                    | Description                                          | Examples returning true     |
|-----------------------------|------------------------------------------------------|-----------------------------|
| Equal (==)                  | true if both sides are                               | `3 == 3` or `3 == '3'`      |
| Not equal (!=)              | true if not equal                                    | `3 != 4`                    |
| Strict equal (===)          | true if equal and same type*                         | `3 === 3` or `"3" === "3"`  |
| Strict not equal (!==)      | true if same type but not equal, or different type   | `3 !== "3"`                 |
| Greater than (>)            | true if left is greater than right                   | `4 > 3` or `"4" > 3`        |
| Greater than or equal (>=)  | true if left is greater than or equal to right       | `4 >= 3` or `3 >= 3`        |
| Less than (<)               | true if left is less than right                      | `3 < 4` or `"3" < 4`        |
| Less than or equal (<=)     | true if left is less than or equal to the right      | `3 <= 4` or `"4" <= 5`      |

(*) - See also [Object.is](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/is) and [sameness](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Equality_comparisons_and_sameness) for more info regarding JS.

*`=>` is not a valid comparison operator, since it is used for [arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions).*

## Loops

### for statements

### while statements

## Answers
