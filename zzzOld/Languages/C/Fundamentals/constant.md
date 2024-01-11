- fixed value variable that cannot be altered by the program during its execution
- written using all caps

```c
const float PI = 3.14159;
printf("Value of pi: %f", PI);
```

if you change the value of pi:
```c
const float PI = 3.14159;
PI = 666;
```
```output
--------------------------------------------------------------------------------
error: assignment of read-only variable 'PI'
```


## macro definition
```c
#include <stdio.h>
#define PI 3.14159
  
int main(void){
    printf("%f", PI);
  
    return 0;
}
```
```console
--------------------------------------------------------------------------------
3.141590
```

```c
#include <stdio.h>
#define PI_SQUARED (3.14159f * 3.14159f)

int main(void){
    printf("%f", PI_SQUARED);

    return 0;
}
```
```console
--------------------------------------------------------------------------------
9.869589
```

## Boolean Values in C89
Since many programs need variables that can store either *false* or *true*. One way to do this is:
```c
int flag;
flag = 0;
flag = 1;
```
Although this works, it doesn't contribute much to program readability. 

To make programs more understandable, use macro definition
```c
#define TRUE 1
#define FALSE 0
```
now it is more readable:
```c
int flag;
flag = TRUE;
flag = FALSE;
```

upgrading this idea further, define a macro that an be used as a type:
```c
#define BOOL int
BOOL flag = TRUE;
```

## Boolean values in C99
C99 provides the \_bool  type: `_Bool flag;`.
```c
_Bool flag;
flag = 1;
flag = 0;
flag = 5; // will be 1(true)
```

another upgrade in C99 is the `<stdbool.h>` header which  provides macros named `true` and `false`. Which will go in a `bool` variable.
```c
#include <stdbool.h>
bool flag = true;
```