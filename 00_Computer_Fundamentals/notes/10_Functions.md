# Functions: Reusability and Modularity (Simple Notes)

## The big idea
Sometimes we need to do the same task many times. Instead of writing the same code again and again, we put it in one place and use it whenever we need it. This is called a **reusable chunk** of code.

**Example:** A washing machine has a "wash" button. You don't wash each cloth by hand. You press the button, and the same steps happen every time.

There are three ways to group code into reusable chunks: functions, methods and modules.

## 1. Functions
A function is a named block of code that does one specific task.

```python
def greet(name):
    print("Hello,", name)

greet("Alice")
greet("Bob")
```
Output:
```
Hello, Alice
Hello, Bob
```

- `def` is the word used to create (define) a function.
- `greet` is the name of the function.
- Writing `greet("Alice")` is called **calling** the function, which makes it run.
- We wrote the task once but used it twice.

## 2. Methods
A method is a function that lives inside a **class**. (Classes belong to object-oriented programming, which you will learn later, so don't worry about the details now.)

```python
class Greeter:
    def greet(self, name):
        print("Hello,", name)

g = Greeter()
g.greet("Alice")
```
Output:
```
Hello, Alice
```
You call a method with a dot: `g.greet("Alice")`.

## 3. Modules
A module is a file that holds related functions, which you can **import** into another file.

File `math_utils.py`:
```python
def add(a, b):
    return a + b
```

File `main.py`:
```python
from math_utils import add

print(add(2, 3))
```
Output:
```
5
```
This keeps your code in separate, tidy files. Python also comes with many ready-made modules.

## Parameters and return values
Two ideas make functions flexible: input and output.

### Parameters = the input
A parameter is a name for a value that the function receives.

```python
def greet(name):      # name is a parameter
    print("Hello,", name)

greet("Alice")        # "Alice" is passed in
```

### Return values = the output
A function can give a result back using `return`.

```python
def add(a, b):        # a and b are parameters
    return a + b      # the result goes back

result = add(3, 5)
print(result)         # 8
```

**Difference between `print` and `return`:**
- `print` only shows something on the screen.
- `return` hands the result back, so you can store it in a variable and use it later.

## Hands-on: greet the user by name
```python
def greet_user(name):
    print("Hello,", name + "!")

greet_user("Alice")
```
Output:
```
Hello, Alice!
```

Pseudocode for the same task:
```
FUNCTION greet_user(name)
    PRINT "Hello, " + name + "!"
END FUNCTION

CALL greet_user("Alice")
```

## Why use functions?
- **Reusability:** write once, use many times.
- **Easy to read:** big programs are split into small, named parts.
- **Easy to fix:** if there is a mistake, you fix it in one place.

## Remember
- A function is a named block of code. Create it with `def` and run it by calling its name.
- Parameters are inputs, and `return` gives the output.
- A method is a function inside a class, and a module is a file of functions you can import.
- Indent the code inside the function, and put a colon after the `def` line.
