Everything in Python is an object like int, string etc.

```python
age = 8 #age has now access to all the properties an object of type int has

print(age.real) #8
print(age.imag) #0, this is not a imaginary number
print(age.bit_length) #4, bit length is the length in binary notation required to represent the number 8
```

```python
items = [1, 2] #items has now access to all the properties an object of type list has
items.append(3) #like this
items.pop() #and this
```
the `.real` , `.imag` , `.bit_length` , `.append()` , `.pop()` are called methods.