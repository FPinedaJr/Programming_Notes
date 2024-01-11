- Inheritance allows us to define a class that inherits all the methods and properties from another class.
- **Parent class** is the class being inherited from, also called **base class**.
- **Child class** is the class that inherits from another class, also called **derived class**.

## Create a Child Class
Create a class named `Student`, which will inherit the properties and methods from the `Person` class:
```python
class Student(Person):  
  pass
```

## Keeping the inheritance
The child's `__init__()` function **overrides** the inheritance of the parent's `__init__()` function.
### Nested `__init__()`
```python
class Student(Person):  
  def __init__(self, fname, lname):  
    Person.__init__(self, fname, lname)
```

### Using the `super()` function
- Python also has a `super()` function that will make the child class inherit all the methods and properties from its parent:
```python
class Student(Person):
  def __init__(self, fname, lname, year):
    super().__init__(fname, lname)
    self.graduationyear = year

student_1 = Student("Mike", "Olsen", 2019)
```
***NOTE:*** The `super()` function is  commonly used.
