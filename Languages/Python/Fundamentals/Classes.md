- Python is an object oriented programming language.
- Almost everything in Python is an object, with its properties and methods.
- A Class is like an object constructor, or a "blueprint" for creating objects.

## Create a Class
To create a class, use the keyword `class`:
```python
class MyClass:  
  x = 5
```

## Create Object Properties/Attributes
### The __init__() Function
- All classes have a function called `__init__()`, which is always executed when the class is being initiated.
- The `__init__()` function is called automatically every time the class is being used to create a new object.

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

p1 = Person("John", 36)

print(p1.name)
print(p1.age)
```

## The __str__() Function
- The `__str__()` function controls what should be returned when the class object is represented as a string.
- If the `__str__()` function is not set, the string representation of the object is returned:
```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def __str__(self):
    return f"{self.name}({self.age})"

p1 = Person("John", 36)

print(p1)
```
```output 
John(36)
```

## Create Object Methods
```python
 def myfunc(self):  
    print("Hello my name is " + self.name)
```
***NOTE:*** The method(function) always have the self parameter.

## The self Parameter
- The `self` parameter is a reference to the current instance of the class, and is used to access variables that belongs to the class.

## Modify Object Properties
```python
p1.age = 40
```

## Delete Object Properties
```python
del p1.age
```

## Delete Objects
```python
del p1
```

