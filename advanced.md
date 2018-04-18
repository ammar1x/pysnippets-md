### Define a class

```python
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
```

### Working with objects

```python
  tomas = Person('Tomas', '11-11-1980') # creating an instance
  tomas.jump() # calling a method
```

### Class Inheritance 1

```python
  Class Employee(Person):
    """Represents an employee"""
    def __init__(self, name, birthDate, role):
      super().___init__(name, birthDate)
      self.role = role
    def getSalary(self):
      return salaries[self.role]
```

### Throw an exception

```python
  def sqrt(x):
    if x < 0:
      raise ValueError("Argument to sqrt cannot be less than 0")
    else:
      # calculate the square root
```


### Catch an exception

```python
  x = -1
  try:
    sqrt(x)
  except ValueError:
    print("oops, an exception occured")
  else: # this block is optional, and it executed only if no exception has occured
    print("It's all good")
  finally: # this block is also optional, and it is used for cleaning up stuff
    print("closing connections with db")
```