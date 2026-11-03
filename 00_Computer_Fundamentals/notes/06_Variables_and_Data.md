# Variables and Data Types in Python (Simple Notes)

## What is a variable?
A variable is a labelled box where you keep data. The box has two parts:
- **Label:** the name of the variable
- **Value:** the data stored inside

```python
my_age = 42
```
Here `my_age` is the label and `42` is the value inside the box.

**Example:** Think of a jar in your kitchen with "Sugar" written on it. The word "Sugar" is the label, and the sugar inside is the value. You can open the jar and change what is inside whenever you want.

## Basic data types
Data comes in different kinds. These are called data types. Python has three basic ones to start with.

| Data type | Meaning | Examples |
|-----------|---------|----------|
| `int` | Whole number, no decimal point | `10`, `-2`, `2025` |
| `float` | Number with a decimal point | `3.14`, `-0.5`, `99.99` |
| `str` | Text, written inside quotes | `"Hello"`, `'Alice'` |

### int (whole numbers)
```python
age = 25
year = 2025
temperature = -5
print(type(age))     # <class 'int'>
```

### float (decimal numbers)
```python
height = 5.9
price = 99.99
print(type(height))  # <class 'float'>
```

### str (text)
```python
name = "Alice"
greeting = 'Hello, world!'
zipcode = "12345"    # still text, because it is in quotes
```
You can use single quotes or double quotes. Anything inside quotes is text, even if it looks like a number.

## Checking the type
Use `type()` to see what kind of data a variable holds.

```python
print(type(25))        # <class 'int'>
print(type(5.9))       # <class 'float'>
print(type("hello"))   # <class 'str'>
```

## Taking input and printing
- `input()` asks the user to type something.
- `print()` shows something on the screen.

```python
name = input("Enter your name: ")
marks = input("Enter your marks: ")

print("Your name is:", name)
print("Your marks is:", marks)
```

Sample run:
```
Enter your name: Ahil
Enter your marks: 98
Your name is: Ahil
Your marks is: 98
```
Whatever the user types is stored in the variable on the left side of `=`.

**Good to know:** `input()` always gives back text (`str`), even when the user types a number. To use it as a number, change it with `int()` or `float()`:
```python
marks = int(input("Enter your marks: "))
```

## Remember
- A variable is a labelled box that stores data.
- The three basic types are `int` (whole numbers), `float` (decimals) and `str` (text).
- Use `type()` to check the type, `input()` to take input and `print()` to show output.
