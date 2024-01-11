allows to group mulitple things in a single name or single list.

### Printing by index
```python
cats = ["meow", "whitey", "spot"]
print(cats[2]) #spot
```

### Replacing by index
```python
cats = ["meow", "whitey", "spot"]
cats[1] = "lola"
print(cats) #["meow", "lola", "spot"]
``` 

### Length of a list
```python
cats = ["meow", "whitey", "spot"]
print(len(cats)) #3
```


### Adding to a list

#### Appending:
```python
cats = ["meow", "whitey", "spot"]
cats.append("lola") #append only takes 1 argument hence you can only add 1 thing
print(cats) #["meow", "whitey", "spot", "lola"]
```

#### Extending:
```python
cats = ["meow", "whitey", "spot"]
cats.extend(["lola", "neko"])
print(cats) #["meow", "whitey", "spot", "lola", "neko"]

## VS

cats = ["meow", "whitey", "spot"]
cats.append(["lola", "neko"])
print(cats) #["meow", "whitey", "spot", ["lola", "neko"]], it will treat the whole thing as 1
```
You can also extend using:
```python
cats = ["meow", "whitey", "spot"]
cats += ["lola", "neko"]
print(cats) #["meow", "whitey", "spot", "lola", "neko"]

# but if you did not include the square brackets [], it will at each letter of a single string

cats = []
string = "youtube" + "whitey"
cats += string
print(cats) #['y', 'o', 'u', 't', 'u', 'b', 'e', 'w', 'h', 'i', 't', 'e', 'y']
```

#### Inserting in the middle of a list
```python
cats = ["meow", "whitey", "spot"]
cats.insert(1, "lola") #inserts lola on index 1
print(cats) #['meow', 'lola', 'whitey', 'spot']
```
Insertine multiple items
```python
cats = ["meow", "whitey", "spot"]
cats[1:1] = ["cat1", "cat2", "cat3"] #3 items
print(cats) #['meow', 'cat1', 'cat2', 'cat3', 'whitey', 'spot']
```


### Removing from a list

remove:
```python
cats = ["meow", "whitey", "spot"]
cats.remove("meow")
print(cats) #['whitey', 'spot']
```

pop:
```python
cats = ["meow", "whitey", "spot"]
print(cats.pop()) #spot, will pop out the last index
print(cats) #['whitey', 'whitey']
```

```python
cats = ["meow", "whitey", "spot"]
print(cats.pop(1)) #whitey, will pop out the index 1
print(cats) #['whitey', 'spot']
```
**Note: the sorted list will be a new list that is different from the original list**

### Sorting a list
```python
cats = ["Meow", "Cat1", "Cat2", "cat3", "whitey", "Spot"]
cats.sort() #will sort the list in an alphabetical order
print(cats) #['Cat1', 'Cat2', 'Meow', 'Spot', 'cat3', 'whitey']
```
It will sort uppercase first before lower case, to fix that:
```python
cats = ["Meow", "Cat1", "Cat2", "cat3", "whitey", "Spot"]
cats.sort(key=str.lower)
print(cats) #['Cat1', 'Cat2', 'cat3', 'Meow', 'Spot', 'whitey']
 ```

Global function `sorted()`
```python
cats = ["Meow", "Cat1", "Cat2", "cat3", "whitey", "Spot"]
print(sorted(cats, key=str.lower)) #['Cat1', 'Cat2', 'cat3', 'Meow', 'Spot', 'whitey']
```



