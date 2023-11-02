good for code reusability.

### Parameter vs Argument

name is the parameter. Ii is on the function definition.
"Meow" and "Spot" are arguments. 
```python
def hello(name): 
	print("hello " + name)

hello("Meow")
hello("Sport")
hello() #this line will cause an error since name has to have a value
```

```python
def hello(name="my cat"): 
	print("hello " + name)
hello() #this line will now not throw and error since the default value of name is already defined
```

You can have more than 1 parameter.
```python
def hello(name, age):
	print(name + " is " + str(age) + " years old.")
hello("Meow", 9) #Meow is 9 years old.
```

### Mutable vs Immutable in function
```python
def change(value):
	value += 2
	
originalValue = 1
change(originalValue)
print(originalValue) #1, since ints are immuable so it cannot be modified instead another variable with the value of 3 will be created but the original val will still be equal to 1.
```

### `return`  function
- The return function will return whatever you want from a function.
- It will acts as the output of the function  and so it will be equivalent to the function.
- The function will end after the return function.
```python
def change(value):
	value += 2
	return value

originalValue = 1
newValue = change(originalValue)
print(newValue) #3, it printed the new value(computed)
```
If you want the function to return nothing, just input a False argument `change(False)`.

You can return more than 1 thing
```python
def hello(name):
	return name, "cat", 8
print(hello("Meow")) #('Meow', 'cat', 8), it will be returned as a tuple
```
### Global and local variable
```python
age = 1 #this age is a global variable since it is declared outside of the function
def hello(birthYear):
	age = 2022 - birthYear #while this age is a local variable
	print(age) #this local age will be different

hello(2020)
print(age) #this global variable
```

if you want the global variable age then you have to:
```python
age = 1 #global variable
def hello(birthYear):
	global age #accessing the global variable
	age = age+(2022 - birthYear)#now age = 1+(2022-2020)
	print(age) #age = 3
  
hello(2020)
print(age) #the global age is also changed
```


### Nested functions [learn more about this]
A nested function is only visible inside that function hence it can only be used in that function.
```python
def count():
	count = 0
	
	def increment():
		nonlocal count
		count += 1
		print(count)
	increment()
count()
```