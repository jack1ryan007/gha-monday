[w3schools-python](https://www.w3schools.com/python/default.asp)

### Variables

Variables are used to store information to be referenced and manipulated in a program. They also provide a way of labeling data with a descriptive name.
```python
name = "Alice"
age = 25
is_student = True
```


### Receiving Input

In Python, you can receive input from the user using the `input()` function.

```python

user_name = input("Enter your name: ")
print("Hello, " + user_name)

```



### Type Conversion

Type conversion refers to changing the data type of a value. You can convert between types using functions like `int()`, `float()`, `str()`, etc.

```python

age = input("Enter your age: ")
age = int(age)  # Convert string to integer
print("You will be " + str(age + 1) + " next year.")

```

### Strings

Strings are sequences of characters enclosed in quotes. You can use single, double, or triple quotes.

```python

greeting = "Hello, World!"
multiline = """This is
a multiline
string."""
print(greeting)
print(multiline)

```

### Arithmetic Operators

Arithmetic operators are used to perform mathematical operations like addition, subtraction, multiplication, division, etc.

```python

a = 10
b = 3
print(a + b)  # Addition
print(a - b)  # Subtraction
print(a * b)  # Multiplication
print(a / b)  # Division
print(a % b)  # Modulus
print(a ** b)  # Exponentiation

```

### Operator Precedence

Operator precedence determines the order in which operators are evaluated.

```python

result = 3 + 5 * 2  # Multiplication before addition
print(result)  # Outputs 13

result = (3 + 5) * 2  # Parentheses change precedence
print(result)  # Outputs 16

```

### Comparison Operators

Comparison operators compare two values and return a boolean value (`True` or `False`).

```python

a = 10
b = 20
print(a == b)  # Equal to
print(a != b)  # Not equal to
print(a > b)   # Greater than
print(a < b)   # Less than
print(a >= b)  # Greater than or equal to
print(a <= b)  # Less than or equal to

```

### Logical Operators

Logical operators (`and`, `or`, `not`) are used to combine conditional statements.

```python

x = True
y = False
print(x and y)  # Logical AND
print(x or y)   # Logical OR
print(not x)    # Logical NOT

```

### If Statements

If statements are used for decision-making operations.

```python

age = 18

if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")

```

### Exercise

Create a simple program that asks for the user's age and prints whether they are a minor, an adult, or a senior (65+).

```python

age = int(input("Enter your age: "))

if age < 18:
    print("You are a minor.")
elif 18 <= age < 65:
    print("You are an adult.")
else:
    print("You are a senior.")

```

### While Loops

A while loop repeatedly executes a block of code as long as a condition is `True`.

```python

count = 0
while count < 5:
    print("Count:", count)
    count += 1

```

### Lists

Lists are ordered collections of items that are mutable (changeable).

```python

fruits = ["apple", "banana", "cherry"]
print(fruits)

```

### List Methods

Python provides various methods to work with lists, such as `append()`, `remove()`, `pop()`, etc.

```python

fruits = ["apple", "banana", "cherry"]
fruits.append("orange")  # Add an item
print(fruits)
fruits.remove("banana")  # Remove an item
print(fruits)

```

### For Loops

For loops iterate over a sequence of elements.

```python

for fruit in ["apple", "banana", "cherry"]:
    print(fruit)

```

### The range() Function

The `range()` function generates a sequence of numbers, which is often used in for loops.

```python

for i in range(5):
    print(i)

```

### Tuples

Tuples are ordered collections of items that are immutable (unchangeable).

``` python

person = ("Alice", 30, "Engineer")
print(person)
print(person[0])  # Accessing elements
```


### Dictionary

Dictionaries in Python are collections of key-value pairs. Each key is unique, and keys are used to store and retrieve values.

```python
# Creating a dictionary
student = {
    "name": "John",
    "age": 21,
    "major": "Computer Science"
}

# Accessing values
print(student["name"])  # Outputs: John
print(student["age"])   # Outputs: 21

# Adding a new key-value pair
student["graduation_year"] = 2024

# Modifying an existing value
student["age"] = 22

# Removing a key-value pair
del student["major"]

# Printing the dictionary
print(student)

```
