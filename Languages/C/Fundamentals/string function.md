- using `#include <string.h>`

```c
char string1[] = "Fernando";
char string2[] = "Pineda";
```

## common string function:
`strlwr(string1)` = lowercase  
	output: string1 == "fernando"

`strupr(string1)` = uppercase => 
	output: string1 == "FERNANDO"

`strcat(string1, string2)` = concatonate/appends string2 to the end of string1
	output: string1 == "FernandoPineda"

`strncat(string1, string2, 3)` = appends *n* characters of string2 to the end of string1
	output: string1 == "FernandoPin"

`strcpy` = copy string2 to string1
	output: string1 == "Pineda"

`strncpy(string1, string2, 3)` = copy *n* characters of string2 to string1
	output: string1 == "Pinnando"

`strset(string1, '?)` = sets all characters of a string to a given character
	output: string1 == "????????"

`strnset(string1, 'x', 3)` = sets the first *n* characters of a string to a given character
	output: string1 == "xxxnando"

`strrev(string1)` = reverses a string
	output: string1 == "odnanreF"

### returns an int
`int result = strlen(string1);` = returns the length of the string
	output: result = 8

**NOTE!** di ko masyadong gets tooooo:
`int result = strcmp(string1, string2);` = string compare all characters
	output: result == 0(if string are the same else result == -1)

`int result = strncmp(string1, string2, 2);` = string compare *n* characters
	output: result = 

`int result = strcmpi(string1, string2);` = string compare all (ignore case)
	output: result = 

`int result = strncmpi(string1, string2, 2)` = string compare *n* character (ignore case)
	output: result = 

