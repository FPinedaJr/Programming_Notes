- like comparison operators in python
- the result of a relational operators are not `true` or `false` 
- instead it is an int value of 1 for true and 0 for false

1. less then (<)
2. greater than (>)
3. less than or equal to (<=)
4.  greater then or equal to (>=)

relational operators can be used to compare integers 
and floating-point numbers like: 1 < 2.5 and 5.6 < 4

The precedence of the relational operators is lower than that of the arithmetic operators: for example, i + j < k -1 means (i + j) < (k -1)

The expression i < j < k is legal in C but since the < opeartor is left associative, the expression means (i < j) < k

## equality operators

1. equal to (==)
2. not equal to (!=)

equality operators have lower precedence than the relational operators so,
	i < j == j < k
is equivalent to
	(i < j) == (j < k)

## Logical operators

1. logical negation (!)
2. logical and (&&)
3. logical or (||)

If the value of the expression can be deduced from the value of the left operand along, then the right operand isn't evaluated.
	(i != 0) && (j / i > 0)
if i is equal to zer, htne the entire expression will be false even without checking for (j / i > 0)


