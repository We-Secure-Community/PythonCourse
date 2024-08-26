# WeSecure.md

## Python course

### Introduction

Python is a high-level programming language, with applications in numerous areas, including web programming, scripting, scientific computing, and artificial intelligence.

#### High level vs low level programming languages

| # | High level language | Low level language |
| --- | --- | --- |
| 1. | It is programmer friendly language. | It is a machine friendly language. |
| 2. | [High level language](https://www.geeksforgeeks.org/difference-between-assembly-language-and-high-level-language/) is less memory efficient. | [Low level language](https://www.geeksforgeeks.org/programming-language-generations/#:~:text=Two%20low%2Dlevel%20languages%20are%20Machine%20Language%20and%20Assembly%20Language.) is high memory efficient. |
| 3. | It is easy to understand. | It is tough to understand. |
| 4. | Debugging is easy. | Debugging is complex comparatively. |
| 5. | It is simple to maintain. | It is complex to maintain comparatively. |
| 6. | It is portable. | It is non-portable. |
| 7. | It can run on any platform. | It is machine-dependent. |
| 8. | It needs compiler or interpreter for translation. | It needs assembler for translation. |
| 9. | It is used widely for programming. | It is not commonly used now-a-days in programming. |
| 10. | It is used in Python, Ruby, etc. | It is used in C, C++, etc. |

#### Language Compilation vs Interpretation

| # | Compilation | Interpretation |
| --- | --- | --- |
| 1. | It translates into machine code before execution. | Translated into machine code at runtime by an interpreter. |
| 2. | It is faster. | It is slower. |
| 4. | It is memory efficient. | It is memory inefficient. |
| 3. | It's less portable, as they are specific to the hardware and operating system of the machine on which they were compiled | It's more portable, as the same source code can be executed on different hardware and operating systems without recompilation. |
| 4. | Compilation errors prevent code from compiling. | Interpreters stop translating the code as soon as they encounter an error. |
| 5. | It is used in C, C++, etc. | It is used in Python, Ruby, etc. |

#### PS Python cloud be compiled for performance

[Python to Binary](https://www.baeldung.com/linux/python-binary)

#### Python

Python is an interpreted, high-level, general-purpose programming language. Created by Guido van Rossum and first released in 1991, Python's design philosophy emphasizes code readability with its notable use of significant whitespace. Its language constructs and object-oriented approach aim to help programmers write clear, logical code for small and large-scale projects.

#### Historial de lanzamientos de Python

| Version | Release Date | End of Life Date |
| --- | --- | --- |
| 1.x | January 1994 | January 2000 |
| 2.x | October 2000 | January 2020 |
| 3.x | December 2008 | - |

### Installation

#### Windows

1. Download the latest version of Python from the [official website](https://www.python.org/downloads/).

2. Run the installer.

3. Check the box that says "Add Python 3.x to PATH".

4. Click on "Install Now".

5. Open the command prompt and type `python --version` to check if Python is installed correctly.

#### Linux

1. Open the terminal.

2. Update the package list.

```bash
sudo apt update
```

3. Install the latest version of Python.

```bash
sudo apt install python3
```

4. Check the installation.

```bash
python3 --version
```

### Basic concepts of Python

#### Reserved words

Python has a set of reserved words that cannot be used as variable names, function names, or any other identifiers.

```python
# There are 33 reserved words in Python 3.9
False      await      else       import     pass
None       break      except     in         raise
True       class      finally    is         return
and        continue   for        lambda     try
as         def        from       nonlocal   while
assert     del        global     not        with
async      elif       if         or         yield
```

#### Lines and Indentation

Python uses indentation to define code blocks, instead of brackets. The standard indentation is 4 spaces.

```python
if 5 > 2:
    print("Five is greater than two!")
```

#### Comments

Python has commenting capability for the purpose of in-code documentation.

```python
# This is a comment
print("Hello, World!")
```
  
  ```python
  """
  This is a comment
  written in
  more than just one line
  """
  print("Hello, World!")
```

#### Variables

Variables are containers for storing data values. Unlike other programming languages, Python has no command for declaring a variable, it's strongly, dynamically typed. This means that the data type of a variable is not explicitly declared but is determined at runtime.

```python
# Strongly typed
1 + "1" # TypeError in Python
1 + "1" // "11" in JavaScript

# Dynamically typed
x = 4
print(type(4)) # at this moment, x points to an integer
x = "Hello, world"
print(type(x)) # and at this moment, x points to a string
```

```python
x = 5
y = "John"
print(x)
print(y)
```

##### Variables and memory

Variables are references to memory locations. When you assign a value to a variable, you are actually binding a reference to a memory location. When you change the value of a variable, you are actually changing the reference to a different memory location.

```python
x = 5
y = x
x = 10

print(x) # 10
print(y) # 5
```

```python
x = [1, 2, 3]
y = x
x[0] = 10

print(x) # [10, 2, 3]
print(y) # [10, 2, 3]
```

```python
x = [1, 2, 3]
y = x.copy()
x[0] = 10

print(x) # [10, 2, 3]
print(y) # [1, 2, 3]
```

```python
x = [1, 2, 3]
y = x[:]
x[0] = 10

print(x) # [10, 2, 3]
print(y) # [1, 2, 3]
```

```python
x = [1, 2, 3]
y = list(x)
x[0] = 10

print(x) # [10, 2, 3]
print(y) # [1, 2, 3]
```

```python
# Get the memory address of a variable
x = 5
print(id(x)) # 1407326744

y = 5
print(id(y)) # 1407326744

x = 10
print(hex(id(x))) # 0x7ff9b1b3b3b0
```

##### Constants

A constant is a type of variable whose value cannot be changed. It is helpful to think of constants as containers that hold information which cannot be changed later.

```python
PI = 3.14
GRAVITY = 9.8
```

##### Multiple assignment

Python allows you to assign values to multiple variables in one line.

```python
x, y, z = "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
```

```python
x = y = z = "Orange"
print(x)
print(y)
print(z)
```

```python
x = "awesome"
print("Python is " + x)
```

```python
x = "Python is "
y = "awesome"
z = x + y
print(z)
```

```python
x = 5
y = 10
print(x + y)
```

```python
x = 5
y = "John"
print(x + y) # TypeError
```

##### Variable names

A variable name must start with a letter or the underscore character. A variable name cannot start with a number. A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _). Variable names are case-sensitive (`age`, `Age`, and `AGE` are three different variables).

```python
myvar = "John"
my_var = "John"
_my_var = "John" # Private variable
myVar = "John"
MYVAR = "John" # Constant
myvar2 = "John"
```

#### Data types

Python has the following data types built-in by default, in these categories:

- Text Type: `str`
- Numeric Types: `int`, `float`, `complex`
- Sequence Types: `list`, `tuple`, `range`
- Mapping Type: `dict`
- Set Types: `set`, `frozenset`
- Boolean Type: `bool`
- Binary Types: `bytes`, `bytearray`, `memoryview`

```python
x = "Hello, World" # str
x = 20 # int
x = 20.5 # float
x = 1j # complex
x = ["apple", "banana", "cherry"] # list
x = ("apple", "banana", "cherry") # tuple
x = range(6) # range
x = {"name" : "John", "age" : 36} # dict
x = {"apple", "banana", "cherry"} # set
x = frozenset({"apple", "banana", "cherry"}) # frozenset
x = True # bool
x = b"Hello" # bytes
x = bytearray(5) # bytearray
x = memoryview(bytes(5)) # memoryview
```

```python
# Setting the specific data type of a variable
x = str("Hello, World")
x = int(20)
x = float(20.5)
x = complex(1j)
x = list(("apple", "banana", "cherry"))
x = tuple(("apple", "banana", "cherry"))
x = range(6)
x = dict(name="John", age=36)
x = set(("apple", "banana", "cherry"))
x = frozenset(("apple", "banana", "cherry"))
x = bool(5)
x = bytes(5)
x = bytearray(5)
x = memoryview(bytes(5))
```

```python
# Get the type of a variable
print(type(x))
```

#### Type casting

You can convert from one type to another with the `int()`, `float()`, `str()`, `list()`, `tuple()`, `set()`, `dict()` constructors.

```python
x = 1 # int
y = 2.8 # float
z = 1j # complex

# convert from int to float:
a = float(x)

# convert from float to int:
b = int(y)

# convert from int to complex:
c = complex(x)

print(a) # 1.0
print(b) # 2
print(c) # 1j
```

#### Operators

Python language supports the following types of operators:

- Arithmetic operators: `+`, `-`, `*`, `/`, `//`, `%`, `**`
- Assignment operators: `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `//=`, `**=`
- Comparison operators: `==`, `!=`, `>`, `<`, `>=`, `<=`
- Logical operators: `and`, `or`, `not`
- Identity operators: `is`, `is not`
- Membership operators: `in`, `not in`
- Bitwise operators: `&`, `|`, `^`, `~`, `<<`, `>>`

```python
x = 5
y = 3

print(x + y) # 8
print(x - y) # 2
print(x * y) # 15
print(x / y) # 1.6666666666666667
print(x % y) # 2
print(x ** y) # 125
print(x // y) # 1
```

#### If...else statement

Python supports the usual logical conditions from mathematics: `==`, `!=`, `>`, `<`, `>=`, `<=`

```python
a = 33
b = 200
if b > a:
    print("b is greater than a")
```

#### While loop

With the `while` loop we can execute a set of statements as long as a condition is true.

```python
i = 1
while i < 6:
    print(i)
    i += 1
```

#### For loop

A `for` loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
    print(x)
```

#### Functions

A function is a block of code which only runs when it is called. You can pass data, known as parameters, into a function. A function can return data as a result.

```python
def my_function():
    print("Hello from a function")

my_function()
```

#### Lambda function

A lambda function is a small anonymous function. A lambda function can take any number of arguments, but can only have one expression.

```python
x = lambda a : a + 10
print(x(5))
```

#### Classes and objects

Python is an object oriented programming language. Almost everything in Python is an object, with its properties and methods. A Class is like an object constructor, or a "blueprint" for creating objects.

```python
class MyClass:
    x = 5

p1 = MyClass()
print(p1.x)
```

#### Inheritance

Inheritance allows us to define a class that inherits all the methods and properties from another class.

```python
class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname

    def printname(self):
        print(self.firstname, self.lastname)

class Student(Person):
    pass

x = Student("Mike", "Olsen")
x.printname()
```

#### Modules

Consider a module to be the same as a code library. A file containing a set of functions you want to include in your application.

```python
import mymodule

mymodule.greeting("Jonathan")
```

```python
import mymodule as mx

a = mx.person1["age"]
print(a)
```

#### File handling

Python has several functions for creating, reading, updating, and deleting files.

```python
f = open("demofile.txt", "r")
print(f.read())
```

```python
f = open("demofile2.txt", "a")
f.write("Now the file has more content!")
f.close()
```

#### Exceptions

When an error occurs, or exception as we call it, Python will normally stop and generate an error message.

```python
try:
    print(x)
except:
    print("An exception occurred")
```

#### User input

Python allows for user input.

```python
username = input("Enter username:")
print("Username is: " + username)
```

### References

- [Python official website](https://www.python.org/)
- [Python documentation](https://docs.python.org/3/)
- [Python for Beginners](https://www.python.org/about/gettingstarted/)
- [Python on W3Schools](https://www.w3schools.com/python/)
- [PEP 8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/)
- [PEP 20 -- The Zen of Python](https://www.python.org/dev/peps/pep-0020/)
