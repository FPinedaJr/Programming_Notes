Create a python program using lambda function to double a specified number(including decimals).

Sample
```
Your Number: 69 (user input)
Doubled Number: 138.0 (console output)
```

```
Your Number: 1.01 (user input)
Doubled Number: 2.02 (console output)
```

# My Answer

inside main.py
```python
doubler = lambda num : num * 2

inputVar = float(input("Your Number: "))
outputVar = doubler(inputVar)
print(f"Doubled Number: {outputVar}")
```

