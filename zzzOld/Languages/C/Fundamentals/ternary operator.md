- shortcut to if/else when assigning/returning a value
- (condition) ? value if true : value if false
- basically this is like the list comprehension of Python

normal if statement:
```c
int greaterNumber(int x, int y){
	if(x > y){
		return x;
	}
	else{
		return y;
	}
}
```

using ternary operator:
```c
int greaterNumber(int x, int y){
	return (x>y) ? x : y;
}
```



