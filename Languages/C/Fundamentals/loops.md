## for loop
- repeats a block of code for a specific amount of times

```c
for(int i=0; i<10; i++){
	code...
	code...
	code...
}
```

## while loop
- repeats a block of code as long as the condition is true
- a while loop may run unlimited times
- a while loop might not execute at all
- checks the condition, THEN execute the block of code

```c
while(condition){
	code...
	code...
	code...
}
```

## do while loop
- always executes a block of code once, THEN checks the condition
- repeats a block of code as long as the condition is true

```c
do{
	code...
	code...
	code...
} while(condition)
```

## nested loop
- a loop inside of another loop

```c
int col;
int row;

printf("Enter the column: ");
scanf("%i", &col);
printf("Enter the row: ");
scanf("%i", &row);

for(int i=0; i<row; i++){
	for(int j=0; j<col; j++){
		printf("#");
	}
	printf("\n");
}
```

# continue vs break

continue = skips rest of code and forces the next iteration of the loop
```c
for(int i=0; i<10; i++){
	if(i == 3){
		continue;
	} else {
	printf("%i-", i);
	}
}
```
```terminal
0-1-2-4-5-6-7-8-9-
```

break = exits a loop/switch
```c
for(int i=0; i<10; i++){
	if(i == 3){
		break;
	} else {
	printf("%i-", i);
	}
}
```
```terminal
0-1-2-
```