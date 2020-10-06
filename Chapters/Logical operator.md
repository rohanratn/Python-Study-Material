 # Logical Operators in Python

### Following are the logical operators

1. and
2. or
3. not

\- Logical operatos can be applied to any type of data.

\- Logical operators works different wirth different datatypes as follows.

## 1. Boolean datatype
\- For boolean arguemetns, result is always a boolean value.

Operator|Result
--------|--------
and| If all arguments are true then result is true
or|If any one of the argument is true then result is true
not| it is the negaton of passed argument

### Example 1:
```
>>> True and True
True
>>> True and False
False
>>> True and True and False
False
>>> 
```

### Example 2:
```
>>> True or False
True
>>> False or False
False
>>> False or True or False
True
>>> 
```

### Example 3:
```
>>> not False
True
>>> not True
False
>>> 
```

## 2. For non boolean datatypes

\- For non boolean arguments, result is always non boolean value.

value|Result
-----|-----
0|False
non-zero|True
Empty String|False

### Example 1: x and y
Condition : if x evaluates to False then return x otherwise return y.
```
>>> 0 and 2
0
>>> 1 and 2
2
>>> 0 and 'python'
0
>>> 1 and 'Python'
'Python'
>>> '' and 1
''
>>> 'python' and 0
0
>>> 
```

### Example 2: x or y
Condition : if x evaluates to True then return x value otherwise return y value.
```
>>> 1 or 0
1
>>> 0 or 1
1
>>> 0 or 0
0
>>> 10 or 20
10
>>> 0 or 'Python'
'Python'
>>> 'python' or 0
'python'
>>> 
```

### Example 3:  not x
Contition : if x value evaluates to True then return False. If it evaluates to False then return True.
```
>>> not 1
False
>>> not 0
True
>>> not 'Python'
False
>>> not ''
True
>>> 
```