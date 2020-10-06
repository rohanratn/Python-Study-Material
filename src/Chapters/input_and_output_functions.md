# Input and Output functions in Python

## Input functions
## input() :

input() function allows user to pass the value at the runtime.

### Note : input() function passes the accepted value in string format only. In order to pass the other datatypes using input(), you need to use [Type Casting Functions](src/Chapters/Type_casting_functions.md).

### Example :
```python
# Passing string value

>>> string=input('Enter a string : ')
Enter a string : Python
>>> print(string)
Python
>>> type(string)
<class 'str'>
>>> 

# Passing integer value

>>> integer=int(input('Enter a number : '))
Enter a number : 20
>>> print(integer)
20
>>> type(integer)
<class 'int'>
>>> 

# Passing float value

>>> float_value=float(input('Enter a float : '))
Enter a float : 3.5
>>> print(float_value)
3.5
>>> type(float_value)
<class 'float'>
>>> 

```

### Take multiple values from single input()
```python
>>> a,b,c,d=[int(x) for x in input().split()]
1 2 3 4
>>> a,b,c,d
(1, 2, 3, 4)
>>> 
```

## eval() :
eval() function takes input in string format converts it to int type

### Example :
```python
>>> eval("1+2*3+4")
11
```

## Output functions
 
