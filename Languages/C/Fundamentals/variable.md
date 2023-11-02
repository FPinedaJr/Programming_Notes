To  make a variable you have to `1. Declare` it and `2. Initialize` it.

```c
int integerVar; //declaration
integerVar = 69; //initialization
```
You can also declare and initilize at the same time:
```c
int integerVar = 69; //declaration + initilization
```

To print the value of a variable, you need to use a placeholder.
To create a place holder use the percent sign + a special character for the variable's datatype.
```c
int age = 18;
float height = 6.9;
char name[] = "Fernando";
printf("Hello, %s\n", name); //%s for string
printf("You are %i years old.\n", age); //%i for integers
printf("You are %f meters tall.", height); //%f for floats
```


## Datatype
Some common datatypes:

### integer
- Whole numbers
```c
int age = 18;
printf("%i", age);
```

### Float
- Decimal numbers
```c
float height = 6.9;
printf("%f", height);
```

### Double
- longer float (for more precise computing)
```c
double doubleVar = 0.12345678900000;
printf("%0.15lf", doubleVar); //lf means long float
```

### Double VS Float
```c
float floatVar = 0.12345678900000;
double doubleVar = 0.12345678900000;
printf("%0.15f\n", floatVar);
printf("%0.15lf", doubleVar);
```
**NOTE!** the default places of decimals to display is 6, `%0.15` is used to change that.

```output
0.123456791043282
0.123456789000000
```

### Char
- Single characters or single letters
```c
char middleName = 'P';
printf("%c", middleName);
```
**NOTE!** you need to enclose chars with single quotes only


### String
**NOTE!** there are no strings in C, instead there is an array of characters
```c
char name[] = "Fernando Pineda Jr.";
printf("%s", name);
```

### Bool
```c
bool alive = true;
printf("%d", alive);
```
**NOTE!** use small letter `true` not `True`.
**NOTE!** You have to put `#include <stdbool.h>` in the header.

### long long int and short
- long long integers are long integers
- it is called 'long long int' because the normal `int` is already 'long int'.
- there is also 'short' for shorter ints.
- this works the same with double as to floats 
- uses `lld` for printing

### unsigned keyword
- an int uses 2 bytes of data.
- a normal `int` can contain numbers from -2,147,483,648 to +2,147,483,647.
- an `unsigned int` can contain numbers from 0 to +4,294,967,295.
