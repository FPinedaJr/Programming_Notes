
### if statement
```c
if(condition){
	code...
	code...
	code...
}
```

### else if statement
```c
else if(condition){
	code...
	code...
	code...
}
```

### else statement
```c
else {
	code...
}
```

### logical operator
- `&&` = and
- `||` = or
- `!variable` = checks if the variable is not true

## example
```c
char grade;

printf("Enter you grade (A,B,C,D,F): ");
scanf("%s", &grade);

if(grade == 'A'){
    printf("\nPerfect!");
}
else if(grade == 'B'){
    printf("\nGreat!");
}
else if(grade == 'C'){
    printf("\nSatisfactory");
}
else if(grade == 'D'){
    printf("\nunsatisfactory");
}

else if(grade == 'F'){
    printf("\nFailed!");
}
else{
    printf("\nThis is not a grade");
}
```

## Conditional Operator
the conditional operator is unique among  C operators in that it requires *three* operands instead of two. For this reason, it is often referred to as a **ternary** operator.

`expr1 ? expr2 : expr3` read as "if expr1 then exr2 else expr3"

its like
```c
if (expr1){
	expr2;
} else {
	expr3;
}
```
