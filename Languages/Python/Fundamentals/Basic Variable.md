- The variable name should start with a lower case character.
- Digits are allowed but variable  name should not start with it.
- Underscore (_) is allowed but this is used for a special type of variable
```python
firstnumber = 5
secondNumber = 15
sum = firstNumber + secondNumber
print("sum")
```

- The id of an object lets you inspect where in the memory is that object stored.
- The id of alpha will be the same with the id of beta to conserve with memory since they contain the vary same value. This is called "object intering" 
```python
alpha = 69
beta = 69
print(id(alpha), id(beta))
```


You can check the type of the variable like:
```python
testVariable = "meow"
print(type(testVariable)==str) #true
print(isinstance(testVariable, str)) #true
```
