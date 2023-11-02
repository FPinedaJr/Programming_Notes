# Arithmetic Operators

```python
plus = 1 + 1 #equals 2
milnus = 2 - 1 #equals 1
times = 2 * 2 #equals 4
devide = 4 / 2 #equals 2
remainder = 4 % 3 #equals 1
power = 4 ** 2 #equals 16
floorDivision = 9 // 2 #equals 3, floor division devides a number and just rounds down
```

The following are the same and will increment the value of `count`  by 1.
```python
count = 0
count += 1 #equals 1
count = count + 1 #equals 2 now
```

# Comparison or Logical Operators

same as operators as mathematics

`a == b`  is when a is **equal** to b
`a != b`  is when a is **not equal** to b
`a < b`  is when a is **less than**** to b
`a > b`  is when a is **greater than** to b
`a <= b`  is when a is **less than or equal** to b
`a >= b`  is when a is **greater than or equal** to b
# Boolean Operators

**IMPORTANT: the value of boolean true  and false is written as `True` and `False`**

`not`  means not that
`and`  means that all conditions should be met
`or`  means that atleast condition should be met
```python
condition1 = true
condition2 = false

not condition1 # will be false
condition1 and condition2 # will be false
condition1 or condition2 # will be true
```

Boolean operator `or` will return the first argument that is **true**.
```python
print(0 or 1) #the first one is false so it will print 1
print(false or "hey") #the first one is false so it will print "hey"
print("Hello" or "Hey") #both are true so it will print the first value, "Hello"
print([] or False) #both are false so it will print the first value, []
print(False or []) #both are false so it will print the first value, False
```

Boolean operator `and` will only evaluate the second argument if the first one is **true**.
This will return the first argument that is false.
```python
print(0 and 1) #The first one if already false so it will print 0
print(1 and 0) #The first one is true so it will proceed and print 0
print (False and "hey") #the first one is already false so it will print, False
print("hi" and "hello") #Both are true so the last one will be printed, "hello"
print([] and False) #Both are false so the first one will be printed, []
print(False and []) #Both are false so the first one will be printed, False
```

# Bitwise Operators

This are rarely used and will only be used on special situations.

`&`  performs binary *AND*
`|`  performs binary *OR*
`^`  performs a binary *XOR* operation
`~`  performs a bilnary *NOT* operation
`<<` shift left operation
`>>`  shift right operation

`is` called the **identity operator**, it is used to compares 2 objects and **returns true** if both are the **same** objects.
`in` called the  **membership operator**, this is used to tell if a **value is contained in** a list or other sequence.
# Ternary Operators

used on conditional statements

normal conditionals are written as:
```python
def isAnAdult(age):
	if age > 18:
		return True
	else: 
		return False
```

Using the ternary operator it can be written as:
```python
def isAnAdult(age)
	return True if age > else False
```
- this is like an if-else statement in a single line and that can be read as pure English.