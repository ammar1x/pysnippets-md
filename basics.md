# Hello World

```python
  print("Hello, World!")
```

# Basic Data Types

Python has the standard basic data types:

* integer: stores whole numbers
* float: stores real values
* string: stores text

## Variable assignment

You don't explicitely specify the type of variable,
as in the case of statically typed programming languages such as Java or C++. Instead, you simply
assign a value to a variable, and Python sets the
type for you.

```python
  i = 1 # assign an integer to i
  s1 = "python" # assign a string to s
  s2 = 'python' # you can use single quotes
  s3 = """this is a multiline string. It
is enclosed in a triple quotes """
  d1 = True # boolean values start with a capital letter
```

To check the data type of a variable, use the `type` function.

```python
  s = "string"
  print(type(s)) # prints <class 'str'>
```

## Conversion between data types

To convert one data type to another, use the `int`, `str`, `float` covertion functions

```python
  i = int(7.8) # returns 7
  i = int("7.8") # int can also take a string
  f = float("7.8") # converts string to float
  s = str(3) # creates a string from 3
```

# Operators

Operators are special symbols, e.g. `+`, which act
on arguments called operands. They are used for
carrying out operations such as arithmetic, comparison, and logical computation.

## Arithmetic Operators

To perform mathemtical operations such as addition
and division, use arithmetical operators.

```python
  i = 7 + 9 # addition
  i = 7 - 9 # subtraction
  # division (Python 3 outputs 0.777, Python 2 outputs 0)
  i = 7 / 9
  # int. division (works the same both in Python 2 & Python 3)
  i = 7 // 9
  i = 7 * 9 # multiplication
  # Modulo operation
  i = 9 % 2 # => 1
  # Exponentiation
  i = 3 ** 4 # => 81
  # To enforce precedence, use parentheses
  i = (1 - 3) * 2 # => -4
```

## Logical Operators

Logical operators work both on boolean and int
operands.

### Boolean Operands

```Python
  x = True
  y = False
  # Logical conjunction, returns false
  z = x and y
  # logical disjunction (alternation), returns true
  z = x or y
  # logical negation, returns false
  z = not x
```

### Integer Operands

```python
  i = 0 and 2  # => 0
  i = -5 or 0  # => -5
  i = 0 == False  # => True
  i = 2 == True  # => False
  i = 1 == True  # => True
```

## Comparison Operators

To compare values, use comparison operators. They
return False or True, depending on the result of
comparison.

### Equality & Inequality

```
# Equality is ==
  i = 1 == 1  # => True
  i = 2 == 1  # => False
  # Inequality is !=
  1 != 1  # => False
  2 != 1  # => True
```

### Greater Than & Less Than

```python
  1 < 10  # => True
  1 > 10  # => False
  2 <= 2  # => True
  2 >= 2  # => True
```

### Comparison Chaining

You can chain comparison operators.
```python
# check if x is between 5 and 6

1 <= x <= 6
```

# Control Flow

Control flow is the order in which statements are executed.

## if Statement

`if` statements are used to carry out different actions based on different conditions.

```python
  year = 2000
  if year == 1000:
    print("Cool")
  elif (year-1000) == 1000:
    print("Happy birthday")
  else:
    print("Not yet")
```

## Loops

To repeat a specific block of code, we use loops.

### for Loop

Iterate from 0 to 99, inclusive:

```python
  for i in range(100):
    print(i)
```

Looping through a list (for-in loop):

```python
  people = ["Adam", "Franck", "Anna", "Tom"]
  for person in people:
    print("Hello, " + person)
```

Looping through a list with indices:

```python
  people = ["Adam", "Franck", "Anna", "Tom"]
  for idx, person in enumerate(people):
    print("%s index is %d" % (person, idx))
```

Looping through a dictionary (for-in loop):

```python
  people = {"Adam": 1, "Franck": 2, "Anna": 3, "Tom": 4}
  for person, items in people.items():
    print("%s has %d items" % (person, item))
```

### `while` Loop

While go through the loop body as long 
as the condition is met.

```python
  i = 0
  while i < 100:
    print(i)
    i += 1
```

# Data structures

From Wikipedia:
> In computer science, a data structure is a particular way of organizing and storing data in a computer so that it can be accessed and modified efficiently. More precisely, a data structure is a collection of data values, the relationships among them, and the functions or operations that can be applied to the data


## List

Lists store items in a specific order.

```python
  cities = [] # create an empty list
  people = ["Adam", "Franck", "Anna", "Tom"]
```
### Accessing elements

To get one element, you use use its index. The index must be an integer.
```python
  i = 1
  f = 2.0
  people[1] # => returns "Franck"
  people[i] # Also legal
  people[f] # You can't do that, throws `TypeError`
```
To get a sublist of a given list, you can use slices.
```python
  list = [1, 2, 3, 4, 5, 6]
  list[1: 3] # => returns [2, 3]
  list[:3] # => you can omit the first index
  list[3:] # => you can also omit the last index
  list[:] # => this creates a copy of a given list
```


### Common List Methods

Let's declare a list, on which we will perform some operations.

```python
  people = ["Adam", "Franck", "Anna", "Tom"]
  person = "James"
```

Add a single element to the end of the list

```python  
  people.append(person)
```

Insert an element at the index 3, shifting elements to the right
```python
  people.insert(3, person)
```

To search for an element use the `index` method. It searches for the given element from the start of the list and returns its index.
It throws a `ValueError` if the element does not appear in that list.
```python
  people.index(person)
```

The 'in' operator searches for a given element without throwing a `ValueError`
```python
  if "Adam" in people:
    print("yes")
  else:
    print("no")
```

The `remove` method searches for the first instance of the given element and removes it (throws ValueError if not present)
```python
peopl.remove("Adam")
```

Sorting and reversing:
```python
  # sort the list in place 
  list.sort() 

  # reverse the list in place 
  list.reverse()

```

## Dictionary
A dictionary (dict) is an key/value collection of pairs, which allows you to associate
a key with a value. In other languages dictionaries are also called maps, hashmaps, or hash tables.


`{}` are used for creating a dictionary.

```python
  # Empty dict 
  people = {}
  # Create and intialize a dict
  people = {'Mark': 1, 'Luke': 2} 
```

### Lookup 

Lookup a value associated with a given key.
If the key isn't found in the dictionary, the dict throws a `KeyError`.
```
  dict = {'Mark': 1, 'Luke': 2}
  dict['Mark'] # => returns 1
```
To test whether a key is in the dictionary without a `KeyError` exception use the `in` operator:
```
  dict = {'Mark': 1, 'Luke': 2}
  if 'Mark' in dict:
    print(dict['Mark'])
``` 

### deletion

To delete a key/value pair, use the `delete` method.
```python
  dict = {'Mark': 1, 'Luke': 2}
  del dict['Mark']
```

# Functions

A function can be roughly understood as a named block of code.

```python
  def add(x, y):
    return x + y
  def subtract(x, y):
    return (x-y)
```

Calling a function:

```python
  add(1, 2) # returns 3
```

# Classes

A class is blueprint for making objects, which hold
data and code for manipulating that data.

```python
  class Person(object):
    def __init__(self, name, birthDate):
      self.name = name
      self.birthDate
    def getBirthDate(self):
      return self.birthDate
    def getName(self):
      return self.name
    def jump(self):
      return self.name + " is jumping"
```

Working with objects:

```python
  tomas = Person('Tomas', '11-11-1980') # creating an instance
  tomas.jump() # calling a method
```
