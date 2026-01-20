# 102_Read_08

- [Expressions and Operators](#expressions-and-operators)
  - [Assignment](#assignment)
    - [Assigning to properties](#assigning-to-properties)
    - [Destructuring](#destructuring)
    - [Evaluation and nesting](#evaluation-and-nesting)
  - [Comparison](#comparison)
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

When a task is expected to repeat until an expected outcome or a limit of attempts is made. Different iteration statements that are available can be found in the Javascript [Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide). Loops, regardless of which type, do practically the same thing, with the same goal in mind; to complete the loop (unless the loop repeats ad infinitum or does not run, essentially broken). Only differing in ways to start and end the loop.

The most coomon loops being:

- [for](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration#for_statement)
- [while](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration#while_statement)

including others such as:

- [do...while](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration#do...while_statement)
- [for...in]()
- [for...of]()
- [labeled]()
- [break]()
- [continue]()

### for statements

Repeats until a specified condition evaluates to false, breaking the loop. Operates very similar to how a for loop would for Java and C.

The structure of a `for` statement is as follows:

``` js
for (initialization; condition; afterthought)
  statement
```

with the steps being:

1. The `initialization` (if any) is executed.
Starting one (or more) counters for the loop, which can be as intricate or complex as needed. Variables can also be declared here.
2. The `condition` is evaluated.
If true, the loop statements execute. If not, loop stops/doesn't run. Assumed true if ommitted from statement.
3. The `statement` executes. Multiple statements can be executed using [block statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/block) `{ }` to group statements together.
4. `afterthought` is executed, if present.
5. Returns to step 2.

### while statements

Executes statement so long as condition evaluates to `true`.  
The structure of a `while` statement looks as such:

``` js
while (condition)
  statement
```

When/if `condition` becomes `false`, the `statement` stops executing and control passes to statement *after* the loop.  

1. The `condition` is tested before `statement` is executed.  
    - If `true`, `statement` is executed and `condition` is tested again.  
    - If `false`, loop exection does not happen and control continues to statement after `while` statement.

Block statement `{ }` can be used to group multiple statements wished to execute.

Avoid infinite loops by ensuring condition eventually becomes `false`.

## Answers

1. What is an expression in JavaScript?
    - a shorthand chosen to represent something else. i.e. `x = 7`, `x` represents `7`.
2. Why would we use a loop while coding?
    - When we want a task to repeat until a condition is met; either correct/expected result or attempts made.
3. When does a `for` loop stop executing?
    - a `for` loop stops executing when when the condition is evaluated to be `false`, thereby breaking/ending the loop. Usually after a set number of attempts.
4. How many times will a while loop execute?
    - Executes so long as the condition is evaluated to be `true`/ Until a condition is met.
