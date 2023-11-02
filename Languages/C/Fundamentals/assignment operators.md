```c
x = 5;            // x is now 5
x = y;            // y is now 5
z = 10 * x + y;   // z is now 55 
```

```c
int x;
float y;

x = 72.99f;    // x is now 72
y = 136;       // y is now 136.0
```

since assignment is an operator, it can be chained.
```c
    int i, j, k, l;
    i = j = k = l = 99;

	/*** WRONG ***/
    int i = j = k = l = 99;
```

an assignment of the form *v = e* is allowed wherever a value of type *v* would be permitted.
```c
x = 1;
z = 1 + (y = x);
printf("%d %d %d\n", x, y, z);   // prints "1 1 2"
```
however this is not a good idea. Embedded assignments can make codes hard to read.

## lvalue
"L-value"
variables are an lvalue

Invalid lvalue in assignment:
```c
12 = x;      /*** WRONG ***/
x + y = 0;   /*** WRONG ***/
-x = y;      /*** WRONG ***/
```

