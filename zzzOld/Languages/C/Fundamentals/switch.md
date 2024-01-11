- A more efficient alternative to using many "else if" statements.
- Allows a value to be tessted for equality against many cases.
- You cannot use switch statements for range of values.
- Default case is not required.
```c
switch(variable){
	case condition:
		code...
		code...
		code...
		break;
	case anotherCondition:
		code...
		code...
		code...
	default:
		code... // else statement
}
```


### using if statement
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

### using switch statement
```c
char grade;

printf("Enter you grade (A,B,C,D,F): ");
scanf("%s", &grade);

switch(grade){
    case 'A':
        printf("\nPerfect!");
        break;
    case 'B':
        printf("\nGreat!");
        break;
    case 'C':
        printf("\nSatisfactory");
        break;
    case 'D':
        printf("\nunsatisfactory");
        break;
    case 'F':
        printf("\nFailed!");
        break;
    default:
        printf("\nThis is not a grade");
}
```
**NOTE!** `break;` is a must

To save space, you can put several case labels on the same line:
```c
switch (grade) {
	case 'A': case 'B': case 'C': case 'D':
		printf("Passing");
		break;
	case 'F':
		printf("Failed");
		break;
	default:
		printf("illegal grade");
		break;
}
```

## Parts of a switch statement

### Basic form of a switch statement
```c
switch (expression){
	case constant-expression : statements
	...
	case constant-expression : statements
	default : statements
}
```
- **Controlling expression**. the word `switch` must be followed by an integer expressoin in parenthesis. Characters are treated as integers in C and thus can ba tested in `switch` statements. Floating-point numbers and strings don't qualify, however.
- **Case labels**. Each case begins with a labels of the form `case constant-expression : `
	  A **constand expressoin** is like an ordinary exprssion except that it can't contain variable or function calls, it can only contains constant numbers like 1, 2, 3, 69.
- **Statements**. No braces are required around the statements. The last statement is normally `break`.
	 Duplicate case labels aren't allowed. The order of the cases doesn't matter.

### Break statement
A case label is nothing more than a marker indicating a position within the switch statemeent. Without the `break` (or some other jump statement), control will  flow from one case into the next. 

Since deliberately falling thorugh from one case into the next is rare, it's a good idea to point out any deliberate ommission of break:
```c
switch (grade) {
	case 4: case 3: case 2: case 1:
		num_passing++;
		/* FALL THROUGH */
	case 0: total_grades++;
			break;
}
```
Without the comment, someone might later fixt the "error" by adding an unwanted break

Although the last case in a switch statement never need a break, it is a good practice

