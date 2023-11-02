Create a python program using lambda and function to get the power of a specified number(integer only).

Sample
```
Powers of: 2 (user input)
Your Number: 8 (user input)
8 raised to 2 = 64 (console output)
```

# My Answer

```python
def exponent(n):
    return lambda number : number ** n
    
inputPow = int(input("Powers of: "))
inputNum = int(input("Your Number: "))
powerer = exponent(inputPow)

outputVar = powerer(inputNum)
print(f"{inputNum} raised to {inputPow} = {outputVar}")
```

