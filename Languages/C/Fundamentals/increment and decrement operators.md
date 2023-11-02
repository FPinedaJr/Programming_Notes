```c
i = i + 1; //short
i += 1; //shorter
i++; //shortest
```

### difference between `++i;` and `i++;`

```c
i = 1;
printf("i is %d\n", ++i); // "i is 2"
printf("i is %d\n", i);   // "i is 2"
```

Evaluating the expression `i++` (a post-increment) produces the result `i`, but causes `i` to be incremented afterwards:
```c
i = 1;
printf("i is %d\n", i++); // "i is 1"
printf("i is %d\n", i);   // "i is 2"
```
