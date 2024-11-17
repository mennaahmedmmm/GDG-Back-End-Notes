# Python Notes

## 1. Data Types

### Integers and Floats
```python
age = 21  # Integer
pi = 3.14  # Float
```
- **Integer**: Whole numbers without a decimal point.
- **Float**: Numbers with a decimal point.

---

### Strings
```python
greeting = "Hello, Python!"  # String
```
- **String**: A sequence of characters enclosed in quotes.

---

### Booleans
```python
is_sunny = True  # Boolean (True or False)
```
- **Boolean**: Represents truth values, either `True` or `False`.

---

## 2. Arithmetic Operations
```python
print(5 + 3)  # Addition: 8
print(10 // 3)  # Floor Division: 3
```
- **+**: Addition.
- **//**: Floor division (integer division).

---

## 3. Comparison Operators
```python
print(5 > 3)  # True (5 is greater than 3)
```
- **Comparison Operators**: `>`, `<`, `>=`, `<=`, `==`, `!=`.

---

## 4. Logical Operators
```python
x = True
y = False
print(x and y)  # False
print(not x)    # False
```
- **and**: True if both conditions are true.
- **or**: True if at least one condition is true.
- **not**: Reverses the boolean value.

---

## 5. Input and Output
```python
name = input("Enter your name: ")  # Takes user input
print("Welcome,", name)  # Outputs a greeting
```
- **input()**: Takes user input as a string.
- **print()**: Outputs a value to the console.

### f-strings
```python
age = 21
print(f"My age is {age} years old.")  # Using f-string for formatting
```
- **f-strings**: A way to embed expressions inside string literals using `{}`.

---

## 6. Conditional Statements

### If-Else
```python
x = 10
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is equal to 5")
else:
    print("x is less than 5")
```
- **if-elif-else**: Used for decision-making.

---

## 7. Functions

### Defining Functions
```python
def greet(name="User"):
    return f"Hello, {name}!"

print(greet("Alice"))  # Hello, Alice!
print(greet())         # Hello, User!
```
- **Defining Functions**: Use `def` to create functions.
- **Default Parameters**: If no argument is passed, the default value is used.

---

## 8. Loops

### For Loop
```python
colors = ["red", "green", "blue"]
for color in colors:
    print(color)
```
- **for loop**: Iterates over a collection like a list or range.

---

### While Loop
```python
count = 0
while count < 5:
    print(count)
    count += 1
```
- **while loop**: Repeats as long as the condition is `True`.

---

## 9. List Comprehensions
```python
squares = [x**2 for x in range(1, 6)]
print(squares)  # [1, 4, 9, 16, 25]
```
- **List Comprehensions**: A concise way to create lists.

---

## 10. Data Structures

### Lists
```python
fruits = ["apple", "banana", "cherry"]
fruits.append("date")
fruits.pop(1)  # Removes "banana"
print(fruits[0:3])  # ['apple', 'cherry', 'date']
```
- **List**: An ordered collection.
- **append()**: Adds an element.
- **pop()**: Removes an element by index.

---

### Tuples
```python
coordinates = (10, 20)
print(coordinates[0])  # 10
```
- **Tuple**: An immutable ordered collection.

---

### Sets
```python
numbers = {4, 1, 2, 3, 3}  # Duplicates removed
print(numbers)  # {1, 2, 3, 4}
```
- **Set**: An unordered collection with no duplicate values.

---

### Dictionaries
```python
person = {"name": "Alice", "age": 25}
print(person["name"])  # Alice
person["profession"] = "Engineer"
print(person)  # {'name': 'Alice', 'age': 25, 'profession': 'Engineer'}
```
- **Dictionary**: A collection of key-value pairs.

---

## 11. Modules

### Built-in Modules
```python
import math
print(math.sqrt(16))  # 4.0
```
- **Module**: A file containing Python code (functions, variables).

---

### Renaming Modules
```python
import math as m
print(m.sqrt(36))  # 6.0
```
- **Alias**: You can rename a module when importing using `as`.

---

### Random Module
```python
import random
print(random.randint(1, 10))  # Random integer between 1 and 10
print(random.choice(["red", "green", "blue"]))  # Random color
```
- **random.randint(a, b)**: Generates a random integer between `a` and `b`.
- **random.choice(list)**: Randomly selects an element from a list.

---

### User-defined Modules
Create a file `my_module.py`:
```python
def greet(name):
    return f"Hello, {name}!"

def add(a, b):
    return a + b
```
In your main file:
```python
import my_module

print(my_module.greet("Alice"))  # Hello, Alice!
print(my_module.add(5, 3))  # 8
```
- **User-defined Modules**: A custom file with functions and variables.

---

## **Practice Section**

Here are 3 tasks to help you practice what you've learned:

1. **Create a Simple Calculator**: 
   - Write a program that prompts the user for two numbers and asks for an operation (addition, subtraction, multiplication, division). 
   - Use conditional statements to perform the operation and return the result.

2. **Create a To-Do List**:
   - Implement a to-do list program using a dictionary where each task has a status (`'pending'`, `'completed'`).
   - Allow users to add, update, and remove tasks, and display the list.

3. **Random Quote Generator**:
   - Create a program that selects a random quote from a list of quotes.
   - The program should allow users to add a new quote to the list and show a random quote each time the user runs the program.

---

## **References** :  
- [W3Schools Python Documentation](https://www.w3schools.com/python/)  
- [Python Official Documentation](https://docs.python.org/3/)
- [Python tutorial in 75 min](https://youtu.be/VchuKL44s6E?si=tUHLhVNOGJ4Og1TR) 
