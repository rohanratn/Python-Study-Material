# Bitwise Operators in Python

Following are the bitwise operators

`&, |, ~,^, <<, >>`

\- Bitwise operators can be used with only Integer and Boolean values.

Operator|Condition
---|---
`&`| if both bits are True then result is True
`|`| If any one bit is True then result is True
`^`| x-or. If both bits are different then the result is 1 else 0
`~`| Negation of bits. changes 0 to 1 and 1 to 0
`<<`| Left shift operation
`>>`| Right shift operation

### Example 1:
```
>>> 4 & 5
4
>>> 4|5
5
>>> 4^5
1
>>> 
```
### Explanation :

Binary value of 4 is 100 and binary value of 5 is 101. so 100&101 is 100 which is equivalent to decimal value 4.
Binary values of digits are used to perform bitwise operations.

### Example 2:
```
# Bitwise complement
>>> ~4
-5
>>> 
```

### Exaplanation : 
Binary value of 4 is 1000. complement of 100 is 011. Decimal value of binary 011 is -5.
Ngeative numbers are represent using 2's complement [here](https://www.tutorialspoint.com/two-s-complement).


### Example 3: 
```
# Right shift
>>> 10 << 2
40
>>> 
# Left shift
>>> 10>>2
2
>>> 
```

### Explanation :
10 in binary form is 1010


left shift : 2 zero bits are added in the right side so it becomes 101000 and that is 40 in decimal form.

Left shift : 2 zero bits are added from the left side so it becomes 0010 which is 2 in decimal form.



