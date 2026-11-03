# Decision Making: if / else (Simple Notes)

## What is decision making?
Decision making lets a program choose what to do, based on a condition. A condition is a question that has only two answers: **True** or **False**.

**Example:** If it is raining, take an umbrella. Otherwise, don't. The program does the same kind of thinking.

In Python, we use **conditional statements** for this.

## 1. The `if` statement
Runs a block of code only when the condition is True. If the condition is False, Python skips the block.

```python
if condition:
    # code runs only if the condition is True
```

**Example:**
```python
age = 20
if age >= 18:
    print("You can vote.")
```

## 2. The `if...else` statement
Runs one block when the condition is True, and a different block when it is False.

```python
if condition:
    # code if True
else:
    # code if False
```

**Example:**
```python
temperature = 35
if temperature > 30:
    print("It is hot.")
else:
    print("It is not hot.")
```

## 3. The `if...elif...else` statement
Checks many conditions, one after another. Python stops at the first one that is True.

```python
if condition1:
    # code if condition1 is True
elif condition2:
    # code if condition2 is True
else:
    # code if none are True
```

- `elif` means "else if".
- You can use as many `elif` blocks as you need.
- `else` is optional and runs only when none of the conditions are True.

**Example: grading**
```python
marks = 72
if marks >= 90:
    print("Grade A")
elif marks >= 60:
    print("Grade B")
else:
    print("Grade C")
```
Output: `Grade B`

## Example program: can the user vote?
```python
age = int(input("Enter your age: "))

if age >= 18:
    print("You are eligible to vote.")
else:
    print("You are not eligible to vote yet.")
```

How it works:
1. `input()` asks for the age, and `int()` turns it into a number.
2. Python checks `age >= 18`.
3. If it is True, the first message is printed. If not, the second one is printed.

Sample runs:
```
Enter your age: 20
You are eligible to vote.
```
```
Enter your age: 15
You are not eligible to vote yet.
```

## Rules to remember
- Put a **colon ( : )** at the end of `if`, `elif` and `else` lines.
- **Indent** the code inside each block. Python uses the spaces to know which lines belong together.
- Use `==` to check if two values are equal. A single `=` stores a value, so don't mix them up.

## Remember
- `if` = do this only when the condition is True.
- `if...else` = choose between two paths.
- `if...elif...else` = choose between many paths.
