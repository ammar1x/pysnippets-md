
### Hello World ###

~~~python
  print("Hello, World!")
~~~

### Assign to a variable ###

~~~python
  i = 1 # assign an integer to i
  s1 = "python" # assign a string to s
  s2 = 'python' # you can use single quotes
  d1 = True # boolean values start with a capital letter
~~~


### operators ###

~~~python
  i = 1 # assignment
  i > 1 # greater
  i >= 1 # greater than or equal to
  i <= 1 # less than
  i < 1 # less than or equal to
~~~


### if statements ###

~~~python
  year = 2000
  if year == 1000:
    print("Cool")
  elif (year-1000) == 1000:
    print("Happy birthday")
  else:
    print("Not yet")
~~~


### for loop ###

iterate from 0 to 99, inclusive:
~~~python
  for i in range(100):
    print(i)
~~~

looping through a list (for-in loop):
~~~python
  people = ["Adam", "Franck", "Anna", "Tom"]
  for person in people:
    print("Hello, " + person)
~~~

looping through a dictionary (for-in loop):
~~~python
  people = {"Adam": 1, "Franck": 2, "Anna": 3, "Tom": 4}
  for person, items in people.items():
    print("%s has %d items" % (person, item))
~~~


### while loop ###

iterate from 0 to 99, inclusive:
~~~python
  i = 0
  while i < 100:
    print(i)
~~~

### Lists ###

~~~python
  people = ["Adam", "Franck", "Anna", "Tom"]
  people.append("Michael") # append to a list
~~~


### Tuples ###
Tuples are like lists, except that they are immutable, so their values cannot be changed after initialization
~~~python
  people = ("Adam", "Franck", "Anna", "Tom")
~~~


### Sets ###
A set represent the set data structure, which has 
different implementation than a list, and therefore
different performance characteristics.

~~~python
  people = {"Adam", "Anna"}
  people.add("Anna")
~~~

### Functions ###

Defining a function, which is a piece of code 
with a name:
~~~python
  def add(x, y):
    return x + y
  def subtract(x, y):
    """Subtract two numbers and return their result"""
    return (x-y)
~~~

Calling a function:

~~~python
  add(1, 2) # returns 3
~~~


### Classes ###
A class is blueprint for making objects, which hold
data and code for manipulating that data:

~~~python
  Class Person(object):
    def __init__(self, name, birthDate):
      self.name = name
      self.birthDate
    def getBirthDate(self):
      return self.birthDate
    def getName(self):
      return self.name
    def jump(self):
      return self.name + " is jumping"
~~~

Working with objects:

~~~python
  tomas = Person('Tomas', '11-11-1980') # creating an instance
  tomas.jump() # calling a method
~~~



