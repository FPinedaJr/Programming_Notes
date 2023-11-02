### List of mutable datatypes in Python
1. List
2. Dictionary
3. Set
### List of immutable datatypes in Python
1. Integers
2. Floating point numbers
3. Booleans
4. Strings
5. Tuple

### Immutable vs Mutable

**Immutable**
- Immutable refers to a variables whose internal state cannot be changed
- int is an example of immutable
```python
print("\n---The id of the following are NOT the same even though it refers to the same variable---")
immutable = 100
print(id(immutable))
immutable = 1
print(id(immutable))
```


**Mutable**
- Immutable refers to a variables whose internal state cannot be changed
- list is an example of immutable
```python
print("\n---The id of the following are the SAME since it refers to the same variable---")
mutable = [1,2,3,4,5]
print(id(mutable))
mutable.append(6)
print(id(mutable))
```
