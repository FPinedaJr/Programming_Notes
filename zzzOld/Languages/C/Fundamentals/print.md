## printf( )

```c
printf(string1, expr1, expr2, ...);
```
 
 values displayed can be:
 - constants
 - variables
 - or more complicated expressions

**conversion specifications** - begins with the `%` character. A placeholder representing a value to be filled in during printing.

```c
    int i, j;
    float x, y;

    i = 10;
    j = 20;
    x = 43.2892f;
    y = 5527.0f;

    printf("i = %d, j = %d, x = %f, y = %f\n", i, j, x, y);
```
```console
-----------------------------------------------------------------------------------
i = 10, j = 20, x = 43.289200, y = 5527.000000
```

```C
    int x, y;
    x = 10;
    y = 20;

    printf("%d %d\n", i); /*** WRONG ***/
    printf("%d\n", i, j); /*** WRONG ***/
```



