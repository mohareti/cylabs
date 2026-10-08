# Python 101

***

#### Python Programming Essentials

### Description

This Tutorial introduces the fundamentals of Python programming, encompassing basic to intermediate concepts. To learn and understand about Python operations, package management, object-oriented programming, and more.

### Prerequisites

* Basic understanding of computer operations
* Familiarity with any programming language is helpful but not mandatory

***

### What is Python?

Python is a general-purpose programming language that is interpreted, high-level, and dynamically typed. It is designed to be easy to read and write. Python is popular because it is versatile, has a large community, and is used for a wide variety of applications.

### Python 2 vs. Python 3

Python 2 is the older version of the language, and it is still widely used. However, Python 3 is the newer version, and it is the recommended version to use. Python 3 has a number of improvements over Python 2, including:

* **It is more secure.** Python 3 has a number of security features that are not present in Python 2.
* **It is more consistent.** Python 3 has a more consistent syntax and semantics than Python 2.
* **It is more future-proof.** Python 3 is the future of the language, and it is the version that is being developed by the Python community.

### Setting up the Python environment

To set up the Python environment, you will need to:

1. Download and install the Python interpreter.<https://www.python.org/downloads/>
2. Create a new project directory.
3. Open a terminal window in the project directory.
4. Type the following command to create a new Python file:

```python
print("Hello, Worl")
```

#### Variables and Data Types

Variables are names that refer to values. Python is dynamically-typed, which means you don't declare variable types explicitly.

```python

x = 10          # Integer
y = 3.14        # Floating point
name = "Alice"  # String

```

```python
print(x)
print(y)
print(name)
```

#### Basic Operators and Operands

Python supports various types of operators, which are used to perform operations on values and variables. Here are some basic arithmetic operators:

Operators are the constructs which can manipulate the value of operands. Python language supports the following types of operators.

* Arithmetic Operators
* Comparison (Relational) Operators
* Assignment Operators
* Logical Operators
* Bitwise Operators
* Membership Operators
* Identity Operators

```python

# Arthematic Operations
a = 10
b = 3

# Addition
print(a + b)

# Subtraction
print(a - b)

# Multiplication
print(a * b)

# Division
print(a / b)

```

```python
# Arthematic Operations
integer_variable = 10
float_variable = 20.5
string_variable = "Hello, World!"
boolean_variable = True

# Print the variables and their types
print("Integer variable:", integer_variable, type(integer_variable))
print("Float variable:", float_variable, type(float_variable))
print("String variable:", string_variable, type(string_variable))
print("Boolean variable:", boolean_variable, type(boolean_variable))

# Basic Operators and Operands
# Perform basic arithmetic operations
addition = integer_variable + float_variable
subtraction = float_variable - integer_variable
multiplication = integer_variable * 2
division = float_variable / 3

# Print the results of the operations
print("Addition:", addition)
print("Subtraction:", subtraction)
print("Multiplication:", multiplication)
print("Division:", division)

# String Manipulation
# Concatenation
concatenated_string = string_variable + " Let's learn Python!"
print("Concatenated String:", concatenated_string)

# Repetition
repeated_string = string_variable * 2
print("Repeated String:", repeated_string)

# Writing to a file
with open('output.txt', 'w') as file:
    file.write("This is a sample text written to the file.")

print("File writing operation completed. Check the 'output.txt' file in your Colab files.")

```

#### String Manipulation

String manipulation is one of Python's strengths. Here's some common string manipulation:

```python
# Concatenation
first_name = "Alice"
last_name = "Smith"
full_name = first_name + ' ' + last_name
print(full_name)

# Multiplication
name_repeat = full_name * 3
print(name_repeat)

# Slicing
substring = full_name[1:5]
print(substring)

```

#### Accepting User Inputs

Python allows for user input via the input() function:

```python
# This line will not execute as expected in a non-interactive environment such as a markdown document.
name = input("What is your name? ")
print("It's nice to meet you " + name)

```

### Basic I/O Operations

Reading from and writing to files is a common task in Python programming.

```python
# Open a file for writing and create it if it doesn't exist
with open('/content/sample_data/example.txt', 'w') as file:
    file.write("Hello, world!")
```

The with statement automatically takes care of closing the file once it leaves the block, even in cases of error. I/O operations should always be done carefully to handle potential exceptions such as file not found errors.

```python
# Open a file for reading
with open('/content/sample_data/example.txt', 'r') as file:
    content = file.read()
    print(content)

```

## Python Control Structures

Control structures in Python determine the flow of program execution based on conditions and loops.

### Indentation in Python

Indentation is crucial in Python and is used to define the blocks of code. Consistent spacing is key.

```plaintext
if condition:
    # Indented four spaces or one tab
    execute_code()
```

### Conditional Statements

Conditional statements allow for branching in code execution based on conditions.

#### If Statement

The `if` statement is used to execute a block of code if a condition is true.

```plaintext
if condition:
    # code to execute if condition is true
```

#### Elif Statement

The `elif` (else if) statement is used to check multiple expressions for `True` and execute a block of code as soon as one of the conditions evaluates to `True`.

```plaintext
if condition_a:
    # code to execute if condition_a is true
elif condition_b:
    # code to execute if condition_b is true
```

#### Else Statement

The `else` statement is used to execute a block of code if none of the preceding conditions are true.

```plaintext
if condition:
    # code to execute if condition is true
else:
    # code to execute if condition is false
```

### Logical Operators

Logical operators are used to combine conditional statements:

* `and`: True if both operands are true
* `or`: True if either operand is true
* `not`: True if operand is false (complements the operand)

### Loops

Loops are used for iterating over a sequence (such as a list, tuple, dictionary, set, or string).

#### For Loops

The `for` loop is used to iterate over the elements of a sequence.

```plaintext
for element in sequence:
    # code to execute for each element
```

#### While Loops

The `while` loop executes a set of statements as long as a condition is

````markdown
# Python Control Structures

Control structures in Python determine the flow of program execution based on conditions and loops.

## Indentation in Python

Indentation is crucial in Python and is used to define the blocks of code. Consistent spacing is key.

```plaintext
if condition:
    # Indented four spaces or one tab
    execute_code()
````

### Conditional Statements

Conditional statements allow for branching in code execution based on conditions.

#### If Statement

The `if` statement is used to execute a block of code if a condition is true.

```plaintext
if condition:
    # code to execute if condition is true
```text

#### Elif Statement

The `elif` (else if) statement is used to check multiple expressions for `True` and execute a block of code as soon as one of the conditions evaluates to `True`.

```plaintext
if condition_a:
    # code to execute if condition_a is true
elif condition_b:
    # code to execute if condition_b is true
```text

#### Else Statement

The `else` statement is used to execute a block of code if none of the preceding conditions are true.

```plaintext
if condition:
    # code to execute if condition is true
else:
    # code to execute if condition is false
```text

### Logical Operators

Logical operators are used to combine conditional statements:

* `and`: True if both operands are true
* `or`: True if either operand is true
* `not`: True if operand is false (complements the operand)

### Loops

Loops are used for iterating over a sequence (such as a list, tuple, dictionary, set, or string).

#### For Loops

The `for` loop is used to iterate over the elements of a sequence.

```plaintext
for element in sequence:
    # code to execute for each element
```text

#### While Loops

The `while` loop executes a set of statements as long as a condition is true.

```plaintext
while condition:
    # code to execute while condition is true
```text

### Break and Continue

`break` and `continue` are used inside loops to alter their normal behavior.

#### Break

## Python Control Structures

### Control Structures

Python control structures manage the flow of your code's execution. There are two main types: conditional statements and loops.

### Indentation in Python

Python uses indentation to define blocks of code. All code within the same block must have the same indentation.

```python
if condition:
    # This is a block of code
    pass
```text

### Conditional Statements (if, elif, else)

Conditional statements allow you to execute different blocks of code depending on various conditions.

```python
if condition:
    # Code runs if condition is true
elif another_condition:
    # Code runs if another_condition is true
else:
    # Code runs if above conditions are false
```text

### Logical Operators

Logical operators are used to combine conditional statements.

* `and`: Both conditions must be true
* `or`: At least one condition must be true
* `not`: Inverts the truth value

### Loops (for and while loops)

Loops are used for iterating over a sequence (like a list, tuple, or string) or executing a block of code multiple times.

#### For Loops

For loops iterate over each item in a sequence.

```python
for item in iterable:
    # Code to execute for each item
```text

#### While Loops

While loops repeat as long as a certain boolean condition is met.

```python
while condition:
    # Code to execute while the condition is true
```text

### Break and Continue

`break` and `continue` control the flow of loops.

* `break`: Exit the loop immediately
* `continue`: Skip the rest of the code inside the loop for the current iteration and move on to the next iteration

```python
for item in iterable:
    if some_condition:
        break  # Exit loop
    if another_condition:
        continue  # Skip to next iteration
    # Code to execute for each item
```text

Remember, these are just the basic structures. Python offers more complex control structures and features that you can explore as you become more comfortable with the language.

```python
## Python Control Structures with Examples

## Indentation in Python

## Correct indentation
if True:
    print("This is correctly indented.")

## Incorrect indentation will raise an IndentationError
if True:
  print("This will cause an error.")

```text

```python
## if condition
age = 18
if age >= 18:
    print("You are eligible to vote.")

```text

```python
## if ..else

### Logical Operators

a = True
b = False

if a and b:
    print("Both a and b are True.")
else:
    print("Either a or b is False.")

if a or b:
    print("Either a or b is True.")
else:
    print("Both a and b are False.")

if not a:
    print("a is False.")
else:
    print("a is True.")

```text

```python
## if .. elif
score = 75
if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
  print("Grade: C")
elif score >= 60:
  print("Grade: D")
else:
  print("Grade: F")
```text

```python
## For loop
## Iterating over a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(f"I like {fruit}.")

```text

```python
## while loop
## Using while loop to count down
countdown = 5
while countdown > 0:
    print(countdown)
    countdown -= 1
print("Liftoff!")

```text

```python
## Break and Continue
## Using break
for number in range(1, 11):
    if number == 5:
        break
    print(number)
## Will print numbers 1 to 4 and then break out of the loop

## Using continue
for number in range(1, 11):
    if number % 2 == 0:
        continue
    print(number)
## Will print only odd numbers, as even numbers are skipped

```text

## Data Collections in Python

Python provides several data structures for storing and manipulating collections of data. Understanding these collections is vital for efficient Python programming.

### Lists

A list in Python is an ordered collection of items which can be modified (mutable). Lists are defined using square brackets `[]` and can contain items of different types.

## Data Collections in Python

In Python, there are several built-in data types that can be used to group multiple data together, known as collections. Among these are lists, tuples, sets, and dictionaries. Understanding how to create and iterate over these collections is fundamental in Python programming.

### Lists

A list is an ordered collection of items that are mutable, meaning we can modify them after their creation. Lists are created by placing all the items (elements) inside square brackets `[]`, separated by commas.

#### Example of List Operations:

````python
## Define a list
my_list = [1, 2, 3, 'Python', 'Code']

## Append a new element
my_list.append('New Item')
print(my_list)

## Access elements
first_item = my_list[0]
print(first_item)

## Negative indexing
last_item = my_list[-1]
print(last_item)

## Slicing
sub_list = my_list[1:3]
print(sub_list)

## Length of a list
list_length = len(my_list)
print(list_length)

```python
# Define a list
my_list=[1,2,3,'Python','Code']

# Append a new element
my_list.append('New Item')
print(my_list)

# Access elements
first_item=my_list[0]
print(first_item)

# Negative indexing
last_item=my_list[-1]
print(last_item)

# Slicing
sub_list=my_list[1:3]
print(sub_list)

# Length of a list
list_length=len(my_list)
print(list_length)
````

#### Tuples are similar to lists, but they are immutable, meaning they cannot be changed after they are created. Tuples are defined using parentheses ().

```python
# Define a tuple
my_tuple = (1, 2, 3, 'Python')

# Accessing elements
second_item = my_tuple[1]
print(second_item)

# Length of a tuple
tuple_length = len(my_tuple)
print(tuple_length)

# Tuples are immutable
# my_tuple[1] = 'New Value' # This would raise an error

```

#### Sets

A set is an unordered collection of items where every element is unique (no duplicates). Sets are defined using curly braces {}.

```python
# Define a set
my_set = {1, 2, 3, 'Python'}

# Adding an element
my_set.add('Code')
print(my_set)

# Checking if an element exists
print(2 in my_set)  # Output: True

# Removing an element
my_set.discard(2)
print(my_set)

# Length of a set
set_length = len(my_set)
print(set_length)

# Sets are unordered
# Items may appear in a different order every time you use them

```

**A dictionary in Python is an unordered collection of data in a key:value pair form. A collection of such pairs is enclosed in curly braces {}.**

```python
# Define a dictionary
my_dict = {'name': 'Python', 'type': 'Programming Language'}

# Accessing elements
language_type = my_dict['type']
print(language_type)

# Adding a new key-value pair
my_dict['version'] = '3.8'
print(my_dict)

# Length of a dictionary
dict_length = len(my_dict)
print(dict_length)

# Iterating over dictionary keys
for key in my_dict:
    print(key, my_dict[key])

```

#### iteration over Collections

You can iterate over the elements of a collection using a loop. For dictionaries, you can iterate over the keys, values, or key:value pairs.

```python
# Iterating over a list
for item in my_list:
    print(item)

# Iterating over a tuple
for item in my_tuple:
    print(item)

# Iterating over a set
for item in my_set:
    print(item)

# Iterating over dictionary keys
for key in my_dict:
    print(key)

# Iterating over dictionary values
for value in my_dict.values():
    print(value)

# Iterating over dictionary key-value pairs
for key, value in my_dict.items():
    print(key, value)

```

## Functions in Python

Functions are one of the most important constructs in Python. They allow you to create blocks of code that can be easily executed multiple times, without needing to rewrite the code.

### Defining Functions

A function is defined using the `def` keyword, followed by a function name with parentheses and a colon. The indented block of code following the `:` is executed each time the function is called.

#### Example of Function Definition:

````python
# Define a function
def greet(name):
    print(f"Hello, {name}!")

# Call the function
greet('Alice')

### Function Parameters and Return Values
Functions can take parameters, which are values you pass into the function to be used within it. Functions can also return values back to the caller using the return keyword.

```python
## Example of Function Parameters and Return Values
## Function with parameters and a return value
def add_numbers(num1, num2):
    return num1 + num2

## Call the function and print the result
result = add_numbers(10, 15)
print(result)

````

#### Scope of Variables

Variables defined within a function have a local scope, meaning they can only be accessed within the function. Variables defined outside of any function have a global scope, and can be accessed anywhere in the code.

```python
## Global variable
x = 'global x'

def test():
    # Local variable
    y = 'local y'
    print(y)
    print(x)

test()
## print(y)  # This will raise an error because y is not accessible here

```text

\#Lambda Functions Lambda functions are small anonymous functions defined with the lambda keyword. They can take any number of arguments, but can only have one expression.

```python
## A simple lambda function
multiply = lambda a, b: a * b

## Use the lambda function
print(multiply(5, 6))

```text

```python
square = lambda x: x**2
print(square(5))  # Prints "25", which is the square of 5

```text

\#Modules and Importing A module is a file containing Python code that can define functions, classes, and variables. These modules can then be imported into other Python programs.

```python
## Assume we have a module named `my_module` with a function `greet()`
import my_module

my_module.greet()  # Calls the greet function from the imported module

```text

**When you import a module, Python looks at several places defined in sys.path. It is a list of directory locations.**

**Using the from Keyword**

You can also use the from keyword to import specific functions, classes, or variables from a module.

```python
from my_module import greet

greet()  # Directly calls the greet function without the module's name prefix

```text

## Python Packages and PIP

Python packages and the Python Package Installer (PIP) are fundamental tools for any Python developer. They enable you to easily use and manage additional libraries and dependencies in your Python projects.

### What are Python Packages?

A Python package is a collection of Python modules under a common namespace. In simpler terms, it's a directory that contains a special file named `__init__.py` and can include other modules and subpackages. Packages allow for a hierarchical structuring of the module namespace using dot notation. For example, a package named `my_package` could have a module named `my_module` accessible as `my_package.my_module`.

#### Example of a Python Package:

* my\_package/ init.py
* my\_module.py sub\_package/ init.py another\_module.py

Here, `my_package` is a Python package containing a module `my_module` and a subpackage `sub_package` with a module `another_module`.

### Introduction to PIP (Python Package Installer)

PIP is a package management system used to install and manage software packages written in Python. It connects to an online repository of public packages, called the Python Package Index (PyPI), to download and install packages.

#### Features of PIP:

* Installing Python packages from PyPI.
* Managing package versions.
* Listing installed packages.
* Uninstalling packages.

### Installing Packages with PIP

To install a package using PIP, you use the command `pip install package_name`. PIP downloads the

**package from PyPI and installs it in your Python environment.**

```python
## Examples of Installaing Package
```text

```python
pip install requests
```text

```python
! pip install requests
```text

**Managing Package Versions**

PIP allows you to specify the version of a package you want to install. You can also upgrade or downgrade a package to a specific version.

```python
pip install requests==2.25.1

```text

```python
## upgrading
pip install --upgrade requests

```text

**vritual Environment**

Virtual environments in Python are a tool to keep dependencies required by different projects in separate places. They solve the "Project X depends on version 1.x but, Project Y needs 4.x" dilemma and keep your global site-packages directory clean and manageable.

```python
## Creating a Virtual Environment
python -m venv myenv
## This creates a new virtual environment named myenv.
## on Unix or Mac OS
## source myenv/bin/activate

```text

```python
## deactivate the virtual env
deactivate
#This command will return you to the global Python environment.

#Using virtual environments with PIP ensures that your projects have access to only the packages they need and reduces conflicts between package versions.
```text

## File Operations in Python

Working with files is a common task in many programming projects. Python provides straightforward methods to handle files, which include reading from and writing to files, managing file paths, and handling exceptions.

### Reading from and Writing to Files

Python allows you to read content from a file and write content to a file. This is commonly done using the built-in `open()` function.

#### Reading from a File:

```python
file = open('example.txt', 'r')
content = file.read()
file.close()
print(content)

```text

This opens example.txt in read mode ('r'), reads its content into the variable content, and then closes the file.

```python
file = open('example.txt', 'w')
file.write('Hello, World!')
file.close()
## This opens (or creates if it doesn't exist) example.txt in write mode ('w') and writes a string to it.
```text

**File Paths, Opening and Closing Files**

When working with files, you need to provide the file path, which can be an absolute or relative path.

**Example of File Paths:**

* Absolute Path: /users/example/documents/example.txt
* Relative Path: documents/example.txt

**Opening and Closing Files:**

Files should always be closed after their operations are completed to free up system resources.

```python
file = open('example.txt', 'r')
## Perform file operations
file.close()

```text

**Working with File Modes**

File modes determine the actions you can perform on the file, like reading, writing, or appending.

* 'r' - Read mode
* 'w' - Write mode
* 'a' - Append mode
* 'r+' - Read and write mode

**Handling File Exceptions**

```python
try:
    file = open('non_existent_file.txt', 'r')
    content = file.read()
    file.close()
except FileNotFoundError:
    print("The file does not exist")

```text

### The Context Managers (with statement)

The `with` statement in Python simplifies exception handling by encapsulating common preparation and cleanup tasks in so-called context managers. For file operations, it ensures that the file is properly closed after its suite finishes, even if an exception is raised.

#### Example of Reading with a Context Manager:

````python
with open('example.txt', 'r') as file:
    content = file.read()
    print(content)

This automatically closes example.txt after the nested block of code is executed, even if an exception occurs.

``` python
with open('example.txt', 'w') as file:
    file.write('Hello, Python!')

##### This writes to example.txt and ensures the file is closed properly afterwards.

Using the with statement for file operations is a best practice in Python, as it makes the code cleaner and more readable, and it handles file closing automatically.

# Object-Oriented Programming in Python

Object-Oriented Programming (OOP) is a programming paradigm that uses "objects" – data structures consisting of data fields and methods together with their interactions – to design applications and computer programs.

## Understanding Classes and Objects

- **Class**: A blueprint for creating objects (a particular data structure), providing initial values for state (member variables or attributes), and implementations of behavior (member functions or methods).
  
  ```python
  class MyClass:
      pass

- **Object**: An instance of a class. It can have attributes and behavior defined by its class.

  ```python
  my_object = MyClass()
````

### The self parameter

* `self` represents the instance of the class. It's used to access variables that belong to the class.

  ```python
  class MyClass:
      def my_method(self):
          pass
  ```

### The **init** method and Constructors

* `__init__` is a special method called a constructor, used to initialize a newly created object’s attributes.

  ```python
  class MyClass:
      def __init__(self, attribute):
          self.attribute = attribute
  ```

### Class Methods, Instance Methods, and Static Methods

* **Instance Methods**: Take `self` as the first argument and relate to a specific instance of the class.

  ```python
  def instance_method(self):
      return 'instance method called', self
  ```
* **Class Methods**: Take `cls` as the first argument and can access class variables but not instance variables.

  ```python
  @classmethod
  def class_method(cls):
      return 'class method called', cls
  ```
* **Static Methods**: Do not take `self` or `cls` as the first argument and behave like regular functions, but belong to the class's namespace.

  ```python
  @staticmethod
  def static_method():
      return 'static method called'
  ```

### Inheritance and Polymorphism

* **Inheritance**: Allows a new class to inherit attributes and methods from an existing class.

  ```python
  class BaseClass:
      pass

  class DerivedClass(BaseClass):
      pass
  ```
* **Polymorphism**: Refers to the way in which different object classes can share the same method name, but those methods can act differently based on which object calls them.

  ```python
  class Dog:
      def speak(self):
          return "Woof!"

  class Cat:
      def speak(self):
          return "Meow!"

  # Polymorphism in use
  for animal in [Dog(), Cat()]:
      print(animal.speak())
  ```

This provides an overview of the key concepts of Object-Oriented Programming in Python, which is a powerful paradigm for structuring and organizing code, especially in large programs or when dealing with complex data models.

````

```python
import socket

class PortScanner:
    def __init__(self, target_ip, start_port, end_port):
        self.target_ip = target_ip
        self.start_port = start_port
        self.end_port = end_port

    def scan_tcp_port(self, port):
        try:
            with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
                s.settimeout(1)
                result = s.connect_ex((self.target_ip, port))
                if result == 0:
                    return True
                else:
                    return False
        except:
            return False

    def scan_udp_port(self, port):
        try:
            with socket.socket(socket.AF_INET, socket.SOCK_DGRAM) as s:
                s.settimeout(1)
                s.sendto(bytes("", "utf-8"), (self.target_ip, port))
                s.recvfrom(1024)
                return True
        except:
            return False

    def perform_scan(self):
        for port in range(self.start_port, self.end_port + 1):
            if self.scan_tcp_port(port):
                print(f"TCP Port {port} is open")
            if self.scan_udp_port(port):
                print(f"UDP Port {port} is open")

````

```python

## Example Usage
scanner = PortScanner("192.112.2.26", 21, 443)  # Object creation
scanner.perform_scan()

```text

In this example:

* A `PortScanner` class is defined with methods for scanning TCP and UDP ports.
* An object `scanner` is created from the `PortScanner` class.
* The `perform_scan` method is called on the `scanner` object to perform the port scanning.

**Please Note**:

* UDP scanning is unreliable using this method, as UDP is connectionless and doesn't respond with errors like TCP.
* Scanning networks without permission can be illegal and unethical. Always obtain explicit authorization before scanning any network or system.
* The script's performance can be improved with multithreading or asynchronous I/O, but this simple version is for demonstration purposes.

## Error Handling in Python

Error handling in Python is managed through the use of exceptions. Exceptions are a way of signaling error conditions in a program. Python provides several built-in exceptions, but also allows the creation of custom exceptions.

### Basic Exception Handling

Exception handling in Python is done through the use of `try` and `except` blocks.

* **Try Block**: Encloses the code that might throw an exception.
* **Except Block**: Handles the exception if one occurs in the try block.

  ```python
  try:
      # Code that might raise an exception
      result = 10 / 0
  except ZeroDivisionError:
      # Handling specific exception
      print("Divided by zero!")
  ```text

### Finally Block

The `finally` block is optional and is executed regardless of whether an exception is raised or not. It's typically used for clean-up code.

```python
try:
    # Code that might raise an exception
    result = 10 / 0
except ZeroDivisionError:
    # Handling specific exception
    print("Divided by zero!")
finally:
    # This block is always executed
    print("This is the finally block.")
```text

### Raising Exceptions

You can raise exceptions using the `raise` statement. This is useful for throwing custom errors or re-raising caught exceptions.

```python
x = -1
if x < 0:
    raise ValueError("x must be non-negative")
```text

### Creating Custom Exceptions

Custom exceptions can be created by defining a new class that inherits from the base `Exception` class.

```python
class MyCustomError(Exception):
    """A custom exception class."""
    pass

try:
    # Code that raises the custom exception
    raise MyCustomError("An error occurred")
except MyCustomError as e:
    print(e)
```text

Understanding and properly implementing error handling in Python can greatly improve the reliability and

robustness of your code, allowing for more graceful handling of unexpected situations and better user experiences.

````

## Advanced Topics and Course Wrap-up

As we conclude this Python course, let's delve into some advanced topics that can enhance your Python programming skills and prepare you for more complex projects.

## Comprehensions

Python supports a concise syntax to create new collections based on existing ones.

- **List Comprehensions**: A concise way to create lists.
  ```python
  squares = [x**2 for x in range(10)]
````

* **Dictionary Comprehensions**: Similar to list comprehensions, but for dictionaries.

  ```python
  squares_dict = {x: x**2 for x in range(10)}
  ```
* **Set Comprehensions**: Used for creating sets in a concise way.

  ```python
  even_numbers = {x for x in range(10) if x % 2 == 0}
  ```

### Iterators and Generators

* **Iterators**: Objects that can be iterated over.

  ```python
  iter_obj = iter([1, 2, 3])
  ```
* **Generators**: Simple way to create iterators using functions and the `yield` keyword.

  ```python
  def count_up_to(max):
      count = 1
      while count <= max:
          yield count
          count += 1
  ```

### Decorators

Decorators are a powerful way to modify

the behavior of functions or classes.

```python
def my_decorator(func):
    def wrapper():
        print("Something before the function is called.")
        func()
        print("Something after the function is called.")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

say_hello()
```

### Advanced Modules

Python provides a vast standard library that includes several advanced modules:

* **os**: Interacting with the operating system.

  ```python
  import os
  os.listdir('.')
  ```
* **sys**: Accessing variables used or maintained by the interpreter and functions that interact strongly with the interpreter.

  ```python
  import sys
  sys.argv
  ```
* **json**: Working with JSON data.

  ```python
  import json
  json.loads('{"name": "John", "age": 30}')
  ```
* **datetime**: Handling date and time.

  ```python
  from datetime import datetime
  datetime.now()
  ```

```python
```

```python
# Python version
from platform import python_version
print(python_version())
```

### Python Packages

```python
import platform
print(platform.node())
```

```python
platform.processor()
```

```python
platform.machine()
```

```python
platform.uname()
```

```python
import math #package : we need include packages to obtain certain capability
import math

# Rounding a number upwards to its nearest integer
print(math.ceil(1.4))  # Output: 2

# Rounding a number downwards to its nearest integer
print(math.floor(1.4))  # Output: 1

# Square root of a number
print(math.sqrt(16))  # Output: 4.0

# Power of numbers (x^y)
print(math.pow(2, 3))  # Output: 8.0

```

```python
import math

# Radians to Degrees
radians = math.pi / 2
print(math.degrees(radians))  # Output: 90.0

# Degrees to Radians
degrees = 60
print(math.radians(degrees))  # Output: 1.0471975511965976

# Sine, Cosine, and Tangent
angle_in_radians = math.radians(30)
print(math.sin(angle_in_radians))  # Output: 0.5 (Sine)
print(math.cos(angle_in_radians))  # Output: 0.8660254037844387 (Cosine)
print(math.tan(angle_in_radians))  # Output: 0.5773502691896257 (Tangent)

```

#### Requests

```python
import requests

# URL to send the request
url = "https://api.open-meteo.com/v1/forecast?latitude=32.814018&longitude=-96.948891&current=temperature_2m,wind_speed_10m&hourly=temperature_2m,relative_humidity_2m,wind_speed_10m"

# Send a GET request to the URL
response = requests.get(url)

# Print the status code of the response
print(f"Status Code: {response.status_code}")

```

```python
import requests

# URL to send the request
url = "https://api.open-meteo.com/v1/forecast?latitude=32.814018&longitude=-96.948891&current=temperature_2m,wind_speed_10m&hourly=temperature_2m,relative_humidity_2m,wind_speed_10m"

# Send a GET request to the URL
response = requests.get(url)

# Print the status code and response content
print(f"Status Code: {response.status_code}")
print(f"Response Content:\n{response.text}")

```

```python
import requests
import json

# URL to send the request
url = "https://api.open-meteo.com/v1/forecast?latitude=32.814018&longitude=-96.948891&current=temperature_2m,wind_speed_10m&hourly=temperature_2m,relative_humidity_2m,wind_speed_10m"

# Send a GET request to the URL
response = requests.get(url)

# Check if the request was successful
if response.status_code == 200:
    # Parse JSON response and print it in a formatted way
    data = response.json()
    formatted_json = json.dumps(data, indent=4)
    print(formatted_json)
else:
    print(f"Error: Status code {response.status_code}")

```

```python
import requests
import json
import csv

# URL to send the request
url = "https://api.open-meteo.com/v1/forecast?latitude=32.814018&longitude=-96.948891&current=temperature_2m,wind_speed_10m&hourly=temperature_2m,relative_humidity_2m,wind_speed_10m"

# Send a GET request to the URL
response = requests.get(url)

# Check if the request was successful
if response.status_code == 200:
    # Parse JSON response
    data = response.json()

    # Extract hourly data
    hourly_data = data.get('hourly', {})
    hourly_temp = hourly_data.get('temperature_2m', [])
    hourly_humidity = hourly_data.get('relative_humidity_2m', [])
    hourly_wind_speed = hourly_data.get('wind_speed_10m', [])
    time = hourly_data.get('time', [])

    # Create and write data to CSV
    with open('/content/sample_data/weather_data.csv', 'w', newline='') as file:
        writer = csv.writer(file)
        writer.writerow(["Time", "Temperature (°C)", "Relative Humidity (%)", "Wind Speed (m/s)"])

        for i in range(len(time)):
            writer.writerow([time[i], hourly_temp[i], hourly_humidity[i], hourly_wind_speed[i]])

    print("Data saved to CSV successfully.")
else:
    print(f"Error: Status code {response.status_code}")

```

```python
import pandas as pd

# Read the CSV file into a DataFrame
df = pd.read_csv('/content/sample_data/weather_data.csv')

# Display the DataFrame
df

```

```python
!pip install pandas matplotlib seaborn

```

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

```python
df['Time'] = pd.to_datetime(df['Time'])

# Plotting
plt.figure(figsize=(10, 6))

# Plot Temperature
plt.subplot(3, 1, 1)
sns.lineplot(x='Time', y='Temperature (°C)', data=df)
plt.title('Temperature over Time')
plt.xlabel('')
plt.ylabel('Temperature (°C)')

# Plot Relative Humidity
plt.subplot(3, 1, 2)
sns.lineplot(x='Time', y='Relative Humidity (%)', data=df)
plt.title('Relative Humidity over Time')
plt.xlabel('')
plt.ylabel('Relative Humidity (%)')

# Plot Wind Speed
plt.subplot(3, 1, 3)
sns.lineplot(x='Time', y='Wind Speed (m/s)', data=df)
plt.title('Wind Speed over Time')
plt.xlabel('Time')
plt.ylabel('Wind Speed (m/s)')

plt.tight_layout()
plt.show()
```
