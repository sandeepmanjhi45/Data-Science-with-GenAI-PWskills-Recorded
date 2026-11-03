# Simple Math and Operators in Python (Simple Notes)

## What is an operator?
An operator is a symbol that tells Python to do something with values. The values it works on are called **operands**.

```python
4 + 2
```
Here `+` is the operator, and `4` and `2` are the operands.

## Types of operators in Python
Python has seven kinds. We start with arithmetic, and learn the others later.

| Type | What it does | Example |
|------|--------------|---------|
| Arithmetic | Maths | `4 + 2` |
| Assignment | Stores a value | `x = 5` |
| Comparison | Compares two values | `x > 3` |
| Logical | Combines conditions | `and`, `or`, `not` |
| Bitwise | Works on 0s and 1s | `&`, `\|` |
| Membership | Checks if something is inside | `"a" in "cat"` |
| Identity | Checks if two names point to the same object | `x is y` |

## Arithmetic operators

| Operator | Meaning | Example | Result |
|----------|---------|---------|--------|
| `+` | Add | `4 + 2` | 6 |
| `-` | Subtract | `4 - 2` | 2 |
| `*` | Multiply | `4 * 2` | 8 |
| `/` | Divide | `4 / 2` | 2.0 |
| `%` | Remainder (modulus) | `5 % 2` | 1 |
| `**` | Power (exponent) | `5 ** 2` | 25 |
| `//` | Floor division (drops the decimal part) | `5 // 2` | 2 |

Things to remember:
- `/` always gives a decimal answer (a float), so `4 / 2` is `2.0`.
- `%` gives what is left over after dividing. `5 % 2` is 1, because 5 = 2 + 2 + 1.
- `//` rounds down. So `5 // 2` is 2, and `-5 // 2` is -3.

**Example:** You have 17 sweets to share among 5 friends.
```python
print(17 // 5)   # 3  -> each friend gets 3 sweets
print(17 % 5)    # 2  -> 2 sweets are left over
```

## What is an expression?
An expression is a mix of values, variables and operators that Python works out to give a result.

```python
a = 10
b = 5
result = a + b    # result is 15
```
`a + b` is the expression.

## Adding two numbers from the user
```python
num1 = int(input("Enter the first integer: "))
num2 = int(input("Enter the second integer: "))

total = num1 + num2
print("The sum is:", total)
```
- `input()` gives text, so `int()` changes it into a whole number.
- Tip: I used the name `total` instead of `sum`, because `sum` is already a built-in Python function and it is better not to reuse that name.

## Order of operations
When an expression has many operators, Python follows an order. This is called **operator precedence**. The top ones run first.

| Order | Operators | Meaning |
|-------|-----------|---------|
| 1 | `( )` | Brackets |
| 2 | `**` | Power |
| 3 | `+x`, `-x`, `~x` | Plus or minus sign, bitwise NOT |
| 4 | `*`, `/`, `//`, `%` | Multiply, divide, remainder |
| 5 | `+`, `-` | Add, subtract |
| 6 | `<<`, `>>` | Bitwise shift |
| 7 | `&` | Bitwise AND |
| 8 | `^` | Bitwise XOR |
| 9 | `\|` | Bitwise OR |
| 10 | `==`, `!=`, `>`, `<`, `>=`, `<=`, `is`, `in` | Comparisons |

(Logical operators `not`, `and` and `or` come after comparisons.)

**Examples:**
```python
print(2 + 3 * 4)     # 14, because * runs before +
print((2 + 3) * 4)   # 20, because brackets run first
print(10 - 4 + 2)    # 8, same level so it goes left to right
```
**Easy way to remember:** use brackets whenever you are unsure. It also makes your code easier to read.

## Remember
- An operator is a symbol that does an action, and operands are the values it works on.
- `/` gives a decimal, `//` drops the decimal part and `%` gives the remainder.
- Brackets run first, then power, then multiply and divide, then add and subtract.
