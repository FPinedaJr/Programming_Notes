- uses the `scanf()` function

```c
int age;
printf("How old are you? ");
scanf("%i", &age);
  
printf("You are %i years old", age);
```
**NOTE!** you need the ampersand(&) symbol for inputs. This is known as address of operator.

To get the input for string, you need to use an array and specify the size of that array.
```c
char name[8];
printf("Enter you name: ");
scanf("%s", &name);

printf("Hello, %s", name);
```
```terminal
-------------------------------------------------------------------------------
Enter you name: Fernando 
Hello, Fernando
-------------------------------------------------------------------------------
Enter you name: Fernando Pineda Jr.
Hello, Fernando
```
**NOTE!** `scanf()` function cannot read any white spaces.

```c
char name[8];
printf("Enter you name: ");
fgets(name, 8, stdin);

printf("Hello, %s", name);
```
```terminal
-------------------------------------------------------------------------------
Enter you name: meow meow
Hello, meow me
```
**NOTE!** sine the array size was set to 8, it can only contain 8 characters

To fix this
```c
char name[72];
printf("Enter you name: ");
fgets(name, 72, stdin);

printf("Hello, %s", name);
```
```terminal
-------------------------------------------------------------------------------
Enter you name: Fernando Pineda jr.
Hello, Fernando Pineda jr.
```
**NOTE!** one drawback of this function is it always include `\n` (newline) after the input
```c
char name[72];
printf("Enter you name: ");
fgets(name, 72, stdin);

printf("Hello, %s, Welcome to meow!", name);
```
```terminal
Enter you name: Fernando Pineda Jr.
Hello, Fernando Pineda Jr.
, Welcome to meow!
```

To fix this
```c
#include <string.h>

char name[72];
printf("Enter you name: ");
fgets(name, 72, stdin);
name[strlen(name)-1] = '\0';

printf("Hello, %s, Welcome to meow!", name);

```
```terminal
-------------------------------------------------------------------------------
Enter you name: Fernando Pineda Jr.
Hello, Fernando Pineda Jr., Welcome to meow!
```


