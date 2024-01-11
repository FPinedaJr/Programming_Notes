The true and false in a boolean starts with a capital like
```python
bool1 = True
bool2 = False
```

Numbers are always true except **zero**.
Strings are always true except when it is empty.
lists, tuples, dictionaries are always true except whan it is empty.

### Any function
the any function will return a value of true when any of the values in an iterable element such as list, tuple and dict are true.
```python
bool1 = True
bool2 = False

test = any([bool1, bool2]) 
print(test) #True
print(type(test)) #bool
```


### All function
This will only return a value of true when all of the values in an iterable element like list, tuple are true.
```python
bool1 = True
bool2 = False

test = all([bool1, bool2]) 
print(test) #False
print(type(test)) #bool
```

