# Debugging and Common Pitfalls (Simple Notes)

## What is debugging?
Debugging means finding and fixing mistakes in your code, so the program works the way you want.

- A **bug** is a mistake in a program that gives a wrong result or makes it behave in a strange way.
- Debugging is not only fixing typing mistakes. It also means understanding and fixing mistakes in your thinking (logic).

**Example:** If your torch does not light up, you check the battery, the bulb and the switch one by one until you find the problem. Debugging works the same way.

## Common types of bugs

| Type | What it means | Example |
|------|---------------|---------|
| **Syntax error** | The code breaks the rules of the language, so Python cannot even start | A missing colon `:` after `if x > 0` |
| **Runtime error** | The code starts, but fails while running | Dividing a number by zero |
| **Logic error** | The code runs without any error, but gives the wrong answer | Using the wrong formula |

**Example of a logic error:** You want the average of two numbers, but you write this:
```python
a = 10
b = 20
average = a + b / 2
print(average)    # 20.0, but the correct answer is 15.0
```
Python did not complain, because the code is valid. But `/` runs before `+`, so the result is wrong. The fix is brackets: `(a + b) / 2`.

## Handling exceptions in Python
An error that happens while the program is running is called an **exception**. If we do nothing, the program crashes. With `try` and `except`, we can handle the error politely.

```python
def divide(a, b):
    try:
        return {"success": True, "result": a / b}
    except ZeroDivisionError:
        return {"success": False, "error": "Cannot divide by zero."}
    except Exception as e:
        return {"success": False, "error": str(e)}
```

How it works:
- Python first **tries** the code inside `try`.
- If a `ZeroDivisionError` happens, the matching `except` block runs.
- If any other error happens, the last `except Exception as e` catches it, and `str(e)` turns the error into a message.

**Example use:**
```python
print(divide(10, 2))   # {'success': True, 'result': 5.0}
print(divide(10, 0))   # {'success': False, 'error': 'Cannot divide by zero.'}
```

## Normalizing errors
Normalizing errors means giving every error the **same standard shape**, whatever caused it. In the code above, every result has the same keys: `success` and either `result` or `error`.

Why this helps:
- **Consistency:** all errors look the same.
- **Logging:** it is easier to store and study errors.
- **Testing:** a standard format makes it simple to check for expected errors.
- **User experience:** the user sees clean, readable messages instead of a crash.

## Reading error messages (traceback)
When Python crashes, it prints a **traceback**. It tells you four things:
1. **Where** the error happened (file name and line number)
2. **What** function or line caused it
3. **What type** of error it was (for example `TypeError` or `ZeroDivisionError`)
4. **Why** it happened (the error message)

**Example:**
```python
def divide(x, y):
    return x / y

divide(10, 0)
```
Output:
```
Traceback (most recent call last):
  File "example.py", line 4, in <module>
    divide(10, 0)
  File "example.py", line 2, in divide
    return x / y
ZeroDivisionError: division by zero
```

How to read it:
- Start from the **last line**. It names the error: `ZeroDivisionError: division by zero`.
- The lines above it show the path to the problem: it began at line 4, and the error happened on line 2 inside `divide`.

## Simple debugging strategies
1. **Use `print()` statements.** Print the values of variables at different points to see what is really happening.
   ```python
   a = 10
   b = 20
   print("a =", a, "b =", b)
   print("result =", (a + b) / 2)
   ```
2. **Check the code step by step.** Go through it one line at a time and ask: "What should this line do?"
3. **Read the error carefully.** The message usually tells you the line and the reason.
4. **Set breakpoints.** A breakpoint pauses the program at a chosen line, so you can look at the values and move forward one step at a time. Code editors such as VS Code have this feature.

## Remember
- A bug is a mistake, and debugging is finding and fixing it.
- There are three kinds: syntax errors, runtime errors and logic errors.
- Read the traceback from the last line upward.
- Use `try` and `except` to handle errors without crashing the program.
- When stuck, `print()` your values and check step by step.
