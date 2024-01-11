are immutable group of objects meaning that once it was created then it cannot be modified unlike list, youcannot add nor remove items in tuple.

it uses parenthesis instead of square brackets.
```python
cats = ("Meow", "Cat1", "Cat2", "cat3", "whitey", "Spot")
print(cats) #['Cat1', 'Cat2', 'Meow', 'Spot', 'cat3', 'whitey']
```

Things you can do in tuple that are the same with list:
- Use indexes `cats[0]`
- length of the tuple `len(cats)`
- Searching in a tuple `print("Meow" in cats) #True`
- Use index ranges `cats[:2]`
- Use the sorted function `print(sorted(cats, key=str.lower)` , this will create a new tuple but not **modiify** the first tuple


