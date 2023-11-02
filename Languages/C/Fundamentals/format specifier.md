format specifier % = defines and formats a type of data to be displayed

some common format specifiers:
`%c` = characters
`%s` = string or array of characters
`%f` = float
`%lf` = double
`%d` or `%i` = integer

`%.1` = decimal precision
`%1` = minimum field width
`$-` = left align

the main difference between `%i` and `%d`, is that the former can be used for decimals, octals 
(`O56`), and hexadecimal(`Ox56`) while the letter can only be used for decimals hence the letter d.

## Example

```c
float item1 = 5.75;
float item2 = 10.00;
printf("Item 1: $%f\n", item1);
printf("Item 2: $%f", item2);
```
```output
-------------------------------------------------------------------------------
Item 1: $5.750000
Item 2: $10.000000
```

With decimal precision
```c
float item1 = 5.75;
float item2 = 10.00;
printf("Item 1: $%.2f\n", item1);
printf("Item 2: $%.2f", item2);
```
```output
-------------------------------------------------------------------------------
Item 1: $5.75
Item 2: $10.00
```

With minimum field width
```c
float item1 = 5.75;
float item2 = 10.00;
printf("Item 1: $%10.2f\n", item1);
printf("Item 2: $%10.2f", item2);
```
```output
-------------------------------------------------------------------------------
Item 1: $      5.75
Item 2: $     10.00
```

With left align
```c
float item1 = 5.75;
float item2 = 10.00;
printf("Item 1: $%-10.2f\n", item1);
printf("Item 2: $%-10.2f", item2);
```
```output
-------------------------------------------------------------------------------
Item 1: $5.75      
Item 2: $10.00
```

