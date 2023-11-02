## Logical Operators
same as operators as mathematics

`a == b`  is when a is **equal** to b
`a != b`  is when a is **not equal** to b
`a < b`  is when a is **less than**** to b
`a > b`  is when a is **greater than** to b
`a <= b`  is when a is **less than or equal** to b
`a >= b`  is when a is **greater than or equal** to b

## Basics of if statement
```python
a = 69
b = 169
if  b > a:
	print("b is greater than a")
```
	The code above will output the "b is greater than a" since 169 is greater than 69.

**Note:** be careful with the indentation, if you just type:
```python
if a = b
print("a is equal to be")
```
You will get an error.

### if-elif-else statement
`if`  is the primary condition.  `elif`  means else if, is the secondary condition. `else`  is the tertiary condition.

```python
if a > b:
	print("a is greater than b")
elif a < b:
	print("a is NOT greater than b then a is less than b")
else:
	print("if a is not greater than nor less than b then it must be equal to b")
```
**Note:** You can have more than one `elif`. However You can only have one `if`  and `else`  statement.