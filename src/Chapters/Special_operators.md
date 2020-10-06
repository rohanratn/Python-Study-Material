# Indentity Operator - is, is not

Identity operators are used to compare the objects, not if they are equal, but if they are actually
the same object, with the same memory location.

### Example :
```python
>>> a=10
>>> b=10
>>> a is b
True
>>> id(a)
1804838976
>>> id(b)
1804838976
>>> 
```
### Note : Python supports reusability of integer objects till limit of 256 only. Where as String objects are always reusable

### Example :
```python
>>> a=256
>>> b=256
>>> a is b
True
 
>>> a=257
>>> b=257
>>> a is b
False

>>> id(a)
48384928
>>> id(b)
48385920
 
>>> a=257
>>> b=257
>>> a is not b
True
 
>>> a='Python'
>>> b='Python'
>>> a is b
True

>>> c='Python'
>>> a is c
True
```


# Membership Operators - in, not in


Membership operators are used to test if a sequence is presented in an object.

### Example :
```python
>>> list1=[1,2,3,4]
>>> 1 in list1
True
>>> 6 in list1
False
>>> 6 not in list1
True
>>> 
```

