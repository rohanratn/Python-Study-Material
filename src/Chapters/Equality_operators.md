# Equality Operators in Python

There are only two operators used to compare equality.
1. ==   (equals to)
2. !=   (not equals to)

You can apply equality operators with any type of data.

### Example :
```
>>> a=10
>>> b=20
>>> c=30
>>> d=10
>>> a==b
False
>>> a==d
True
>>> a==b==c
False
>>> a!=b
True
>>> a!=d
False
>>> a!=b==d
False
>>> 
```

### Note :
1. Equality operators compares only content and not address.
2. To compare the address, we have to use 'is' operator.
3. Following are the conditions for equality operator

First value|Second Value|Result
-----------|------------|-------
True|True|True
True|False|False
False|False|True
Flase|True|False

Example :
```
>>> True==True
True
>>> True==False
False
>>> False==False
True
>>> False==True
False
>>> 
```






















