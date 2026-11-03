# Loops: The Idea of Repetition (Simple Notes)

## What is a loop?
A loop repeats the same code many times, so you don't have to write it again and again.

**Example:** Imagine your teacher asks you to write "I will not be late" 100 times. You would not want to write it by hand 100 times. A loop does that for you in just two lines.

## Why do we need loops?
Without a loop, repeating a task means copying the same line:

```python
print("Hello")
print("Hello")
print("Hello")
```

With a loop, it is short and easy to change:

```python
for i in range(3):
    print("Hello")
```
Output:
```
Hello
Hello
Hello
```
If you want 1000 greetings, you only change the 3 to 1000.

## The `for` loop with `range()`
A `for` loop is used when you know how many times to repeat.

`range()` makes a list of numbers to count through. It has one rule to remember: **it stops just before the last number.**

| Code | Numbers it gives |
|------|------------------|
| `range(3)` | 0, 1, 2 |
| `range(1, 6)` | 1, 2, 3, 4, 5 |

### Example: print numbers 1 to 5
```python
for i in range(1, 6):
    print(i)
```
Output:
```
1
2
3
4
5
```
We write `6` and not `5`, because `range` stops before the last number.

Here `i` is just a name for the current number. Each time the loop runs, `i` takes the next value.

## The `while` loop
A `while` loop keeps repeating **as long as a condition is True.** It is useful when you don't know in advance how many times it will run.

### Example: print numbers 1 to 5
```python
i = 1

while i <= 5:
    print(i)
    i += 1
```
Output:
```
1
2
3
4
5
```

How it works, step by step:
1. `i = 1` is the starting value.
2. Python checks `i <= 5`. If it is True, it runs the code inside.
3. `print(i)` shows the number.
4. `i += 1` adds 1 to `i`. It is short for `i = i + 1`.
5. Python goes back to step 2. When `i` becomes 6, the condition is False and the loop stops.

**Warning:** If you forget `i += 1`, `i` never changes, the condition stays True, and the loop runs forever. This is called an **infinite loop**.

## Pseudocode for the same task
```
START
SET i = 1
WHILE i <= 5
    PRINT i
    i = i + 1
END WHILE
END
```

## `for` or `while`?

| | `for` loop | `while` loop |
|---|-----------|--------------|
| Use when | You know how many times to repeat | You repeat until a condition changes |
| Example | Print 1 to 5 | Keep asking until the user types the right password |

## Remember
- A loop repeats code so you don't write it many times.
- `for i in range(1, 6)` gives 1 to 5, because `range` stops before the last number.
- A `while` loop runs as long as its condition is True, so always change something inside it to avoid an infinite loop.
- Indent the code inside the loop, and put a colon after the `for` or `while` line.
