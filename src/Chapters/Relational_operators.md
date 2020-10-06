# Relational Operators in Python

### Following are the relational operators in python

Operator|Purpose
--------|-------
`<`|Less than
`<=` | Less than equal to
`>` | Greater than
`>=` | Greater than equal to

### Example :
```
>>> a=10
>>> b=2
>>> a<b
False
>>> a>b
True
>>> a<=b
False
>>> a>=b
True
>>> 
```

### Note 
1. Relational operators always give boolean result.
2. If relatinal operators are used with string, it will be compared on the basis of alphabetical order and ASCII code will be compared.
```
>>> a='Python'
>>> b='World'
>>> a>b
False
>>> a<b
True
>>> a>=b
False
>>> a<=b
True
>>> 
```
3. If all the arguments passed are thrue then only it returns thrue. If any one argument is false then the result is false.
```
>>> a=10
>>> b=20
>>> c=30
>>> a<b<c
True
>>> a<b>c
False
>>> a>b>c
False
>>> a>c<b
False
>>> 
```
