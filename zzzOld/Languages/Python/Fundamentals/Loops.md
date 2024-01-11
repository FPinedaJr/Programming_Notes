In python  there are 2 types of loops: for loops and while loops.

### Break and Continue

**Continue**
```python
items = [1,2,3,4]
for item in items:
	if item ==2:
		continue
	print(item) #1,3,4. It will skip when item==2 but the code will still continue
```
**Break**
```python
items = [1,2,3,4]
for item in items:
	if item ==2:
		Break
	print(item) #1, the code will break at item==2 so it will not continue 
```


### While loops

This will loop infinitely:
```python
condition = True
while condition == True: #This loop will run infinitely unless you set the value of condition to not True
	print("The condition is still True")
```

while loop that will stop when a certain number of loop is run:
```python
count = 0
while count < 10: #loops are like index it start from 0
	print("This will be printed 10 times")
	count += 1
```
### For loops
- Usually you don't need to define a variable to act as a counter when using for loops.
- Its commonly used to iterate the values in a list.
```python
list = [1,2,3,4,5,6,7,8,9,10]
for item in list: 
	print(item)
```

You can also use a range like:
```python
for item in range(15):
    print(item) #will print 0-14
```

To know the indexes from a for loop:
```python
list = ["Meow", "Spot", "Whitey", "Lola"]
for index, item in enumerate(list): 
	print(index, item)
```