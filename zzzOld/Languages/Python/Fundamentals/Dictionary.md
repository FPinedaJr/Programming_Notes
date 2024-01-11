Dictionaries store in key-value pair.

```python
cat = { "name": "Meow", "age": 5}
cat["name"] = "Spot" #will change the value of name(this is a key) to "spot"
cat[5] = "dog" #this will not change the value of 5(since this is a value) but instead it will create another key with the value "dog"
print(cat) #{'name': 'Spot', 'age': 5, 5: 'dots'}


print(cat)

```

#### `get()`  function
```python
cat = { "name": "Meow", "age": 5}
print(cat.get("name")) #Meow
print(cat.get("color", "black")) #black, however this will not be added to the tuple
print(cat) #{'name': 'Meow', 'age': 5}


#if color is already in the tuple:
cat = { "name": "Meow", "age": 5, "color": "white"}
print(cat.get("color", "black")) #white, since this key is already in the tuple. it cannot modify that

```



#### `pop()`  and `popitem()` function
```python
cat = { "name": "Meow", "age": 5}
print(cat.pop("name")) #Meow, will pop the 
print(cat) #{'age' : 5}
```

```python
cat = { "name": "Meow", "age": 5}
print(cat.popitem()) # {'age': 5}, will remove the last item or last pair
print(cat) #{'name': "Meow"}
```

#### `in`  function
```python
cat = { "name": "Meow", "age": 5}
print("color" in cat) #False
```
#### `keys()` and `values()`  function
```python
cat = { "name": "Meow", "age": 5}
print(cat.keys()) #dict_keys(['name', 'age'])
print(list(cat.keys())) #['name', 'age'], note that this is casted to a list now
```

```python
cat = { "name": "Meow", "age": 5}
print(cat.values()) #dict_values(['Meow', 5])
print(list(cat.values())) #['Meow', 5]
```
### Converting a dict to a list
```python
cat = { "name": "Meow", "age": 5}
print(list(cat.items())) #[('name', 'Meow'), ('age', 5)], just like normal casting
```
### Length of a dict
```python
cat = { "name": "Meow", "age": 5}
print(len(cat)) #2, cause there are only 2 pairs
```


### Appending to a dict
```python
cat = { "name": "Meow", "age": 5}
cat["color"] = "white"
print(cat) #{'name': 'Meow', 'age': 5, 'color': 'white'}
```
### Deleting a pair from a dict
```python
cat = { "name": "Meow", "age": 5}
del cat["age"]
print(cat) #{'name': 'Meow'}
```
### Copying a whole dict
```python
cat = { "name": "Meow", "age": 5}
catCopy = cat.copy()
print(catCopy) #{'name': 'Meow', 'age': 5}
print(cat) #{'name': 'Meow', 'age': 5}
```

