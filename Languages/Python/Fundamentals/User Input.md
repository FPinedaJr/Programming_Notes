
```python
variable = input("Please input something: ")
```
The code will place the input of the user in the variable 'variable' and will store it as of type string by default.

```python
variable = int(input("Enter a whole number: "))
```
The code will  place thje input of the user in the variable 'variable' however this time, it will be stored as an int.

```python
print("Please seperate the numbers with a 'space'")
number1, number2 = map(int, input("Enter two numbers: ").split())
```
The code will request multiple inputs from the user however the you have to seperate them by a space for the `.split()` function to work. 