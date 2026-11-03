# Syntax and Source Code (Simple Notes)

## What is source code?
Source code is the set of instructions that a programmer writes in a programming language. In Python, it is saved in a file that ends with `.py`.

## What is syntax?
Syntax means the rules of a programming language. It is like grammar in English. If you break the rules, the computer cannot understand you.

**Example:** In English, "Me going school" is wrong grammar, so people may not understand it. In the same way, wrong syntax makes Python stop with an error.

## Main syntax rules in Python

| Rule | Example | What it means |
|------|---------|---------------|
| **Indentation** | the space before `print(x)` below | Spaces at the start of a line show which lines belong together |
| **Colon ( : )** | `if`, `for`, `while` and `def` end with `:` | A colon starts a new block of code |
| **Keywords** | `if`, `else`, `def`, `return` | Special words with fixed meaning, so we cannot use them as our own names |
| **Brackets ( )** | `print("Hello")` | Used when calling a function |
| **Quotes and commas** | `'text'`, `("x", "y")` | Quotes mark text, and commas separate items |
| **Assignment ( = )** | `x = 5` | Stores a value in a name |

### Example with indentation and colon
```python
x = 5
if x > 0:
    print(x)
```
The colon after `if x > 0` starts a block. The indented `print(x)` line belongs to that block, so it runs only when `x` is greater than 0.

## A simple Python program
```python
print("Hello, World!")
x = 5
y = 10
print(x + y)
```
Output:
```
Hello, World!
15
```
- `print()` shows something on the screen.
- `x = 5` and `y = 10` store two numbers.
- `x + y` adds them, giving 15.

## Why syntax matters
- If the syntax is wrong, Python will not run your code at all. It shows an error instead.
- Python is very strict about **indentation**. Many other languages are not.

**Example of wrong syntax:**
```python
if x > 0
    print(x)
```
The colon is missing after `if x > 0`, so Python shows a `SyntaxError`.

## Remember
- Source code is what we write, and syntax is the rules we must follow.
- Use a colon to start a block, and indent the lines inside it.
- One small mistake in syntax can stop the whole program.
