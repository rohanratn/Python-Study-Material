# Datatypes in details
	
## int Datatype
\- int is used to represent integral values.

\- long vaues can also be represented by int datatype. 	
	
### There are 4 ways to specify int value
1. Decimal
2. Binary
3. Octal
4. Hexadecimal
---

### Decimal	:
we can use digits from 0 to 9 to specify int value.
```python
>>> a=10
>>> b=20
```
### Binary	:
We need to explicitely declare the binary value using \"0b or 0B\"
```python
>>> a=0b1111
>>> b=0B1111
>>> type(a)
<class 'int'>
```		
Note : When you pass binary to int datatype, it automatically converts binary to int.
```python
>>> a=0b1111
>>> print(a)
15
```
### Octal :
We need to explicitely declare the octal value using \"0o or 0O\".
```python
>>> a=0o1234
>>> b=-O1234
>>> print(a)
668
```
### Hexadecimal :
We neex to explicitely declare the hexadecimal value using \"0x or 0X\".
```python
>>>	a=0xAF
>>> print(a)
175
```
Note :	We can pass input in any form, python will automaticallyconvert it to decimal int value.

## Base conversion functions :
We Can convert base of an int value to any of above type using following functions.
1. **bin()**
2. **oct()**
3. **hex()**
```python	
>>> a=10
>>> bin(a)
'0b1010'
>>> oct(a)
'0o12'
>>> hex(a)
'0xa'
```

## Float Datatype
-	The only way to represent float values is using decimal values.
-	binary, octal, hexadecimal values are not allowed.
```python
>>> f=123.456	# allowed
>>> f= 0b1111	# not allowed
>>> f=0xFACE	# not allowed
>>> f=0o1234	# not allowed
>>> f=123e3		# exponential form is allowed. e3 = 10^3
```				
## Complex Datatype

**format** : a+bj

where,		

	a=real part
	b=imaginary part
	j= underroot -1
Example : 
```python
>>> x=10+2j
>>> type(x)
<class 'complex'>

x=10+2R		# not allowed	
x=10+2i		# not allowed	
x=10+2j		# allowed
x=10+j2		# not allowed	
x=10.2+1j	# allowed
x=a+2j		# allowed
x=10+2.2j	# allowed
```			
To get real and imaginary part of a complex number,
```python
>>> x=10+2j
>>> x.real
10
>>> x.imag
2.0
```
		
## Boolean Datatype
\- Boolean datatype is used to represent boolean values.

\- Allowed values are True and False (first letter of each is capital).

Example :
```python
>>> a=True
>>> b=False
>>> type(a)
<class 'bool'>
>>> a=10
>>> b=20
>>> c=a>b
>>> c
False
>>> a=True
>>> b=False
>>> a+b
1
>>> a*b
0
>>> 
```
### Note : True=1, False=0	

## str Datatype 
\- Any sequence of characters enclosed with single or double quotes is a string.
Example :
```python
>>> s='rohan'
>>> str="Ratnaparkhi"
>>> str
'Ratnaparkhi'
>>> type(s)
<class 'str'>
>>> multi_line='''rohan
ratnaparkhi'''
>>> multi_line
'rohan\nratnaparkhi'
>>> 
```	

### Note :	To consider passed string as a raw string, we can enclose it in thriple single/double quotes.

## Slice operator

**syntax :** str['begin':'end':'step']

Example :
```python
>>> s='rohan ratnaparkhi'
>>> s[1:4]
'oha'
>>> s[1:8]
'ohan ra'
>>> s[:]
'rohan ratnaparkhi'
>>> s[:7]
'rohan r'
>>> s[2:]
'han ratnaparkhi'
>>> s[-1:-4]			# begin should always start from lower index
''
>>> s[-1:]
'i'
>>> s[-4:-1]
'rkh'
>>> s[0:6:2]			# step is optional. it skips the iteration by step value
'rhn'
>>> 
```

## bytes Datatype

\- It represents a group of byte numbers just like an array.

### Note : It can be used for numbers in range of 0 to 256

Example :
```python
>>> a=[1,2,3,4]
>>> b=bytes(a)
>>> b
b'\x01\x02\x03\x04'		# machine readable only
>>> 
```
To print elements 
```python
>>> for i in b : print(i)

1
2
3
4
>>> 
```
We can use only numbers between 0 to 256, otherwise we will get compile time error.
```python
>>> a=[1,2,3,257]
>>> b=bytes(a)
Traceback (most recent call last):
  File "<pyshell#9>", line 1, in <module>
    b=bytes(a)
ValueError: bytes must be in range(0, 256)
>>> 
```

\- Bytes datatype is immutable. We cannot change the contents afterwards.
Example :
```python
>>> a=[1,2,3,4]
>>> b=bytes(a)
>>> b[1]
2
>>> b[1]=6
Traceback (most recent call last):
  File "<pyshell#15>", line 1, in <module>
    b[1]=6
TypeError: 'bytes' object does not support item assignment
>>> 
```

## bytearray Datatype	
	
\- bytearray datatype is exactly same as bytes datatype with only difference that bytearray is mutable.

\- We can change contents of bytearray	
Example :
```python
>>> a=[1,2,3,4]
>>> b=bytearray(a)
>>> b
bytearray(b'\x01\x02\x03\x04')
>>> b[1]
2
>>> b[1]=5
>>> b[1]
5
>>> for i in b: print(i)

1
5
3
4
>>> 
```

## list datatype

\- we can store heterogeneous data elements in a single list

\- Insertion order is preserved and duplicates are allowed in list.

\- List is a mutable datatype. We can change the contents of list.

Syntax :
```python
>>> list_name=[element1, element 2......]
```
### Note : items in list are separated by comma.

Example :
```python
>>> my_list=[1,2,3.4,10+20j]
>>> my_list=[1,2,3.4,10+20j, 'Python']		# Heterogeneous elements
>>> type(my_list)
<class 'list'>
>>> for i in my_list: print(i)

1
2
3.4
(10+20j)
Python
>>> 
```

\- First element is present at list[0] position and last is present at list[-1]

\- List supports negative indexing

Example :
```python
>>> my_list
[1, 2, 3.4, (10+20j), 'Python']
>>> my_list[0]
1
>>> my_list[-1]
'Python'
>>> my_list[-3]
3.4
>>> 
```
We can perform various operations on/with list datatype.
Check [Lists](src/Chapters/List_in_detail.md) chapter. 

## tuple datatype

\- tuple is same as list with only different being it is immutable. We cannot change the content of tuple.

\- Insertion order is preserved in tuple.

\- Duplicates are allowed.

\- Heterogeneous elements are allowed.

**Syntax :** 
```python
tuple_name=() 
```
Example :
```python
>>> my_tuple=(1,2,3.4,True, 'python')
>>> type(my_tuple)
<class 'tuple'>
>>> my_tuple
(1, 2, 3.4, True, 'python')
>>> 
```
\- A tuple can have list as object and that list is muable.
Example :
```python
>>> my_tuple=(1,2,3,[4,5,6,7])
>>> my_tuple
(1, 2, 3, [4, 5, 6, 7])
>>> my_tuple[3][1]
5
>>> my_tuple[3][1]=8      #  changed the content of list
>>> my_tuple
(1, 2, 3, [4, 8, 6, 7])
>>> 
```
We can perform various operations on/with list datatype.
Check [tuple](src/Chapters/Tuple_in_detail.md) chapter. 

## range Datatype

\- Range datatype represent a sequence of values. IT is always immutable. we cannot change the values.

There are 3 format to specify a range.

1. range(end_val)

Example : 
```python
>>> range(10)
range(0, 10)
>>> for i in range(10) : print (i)

0
1
2
3
4
5
6
7
8
9
>>> 
```

### Note : when only one value is given in range function, it starts the range from 0 to passed value.

2. range(start_val,end_val)

Example :
```python
>>> for i in range(10,20) : print (i)

10
11
12
13
14
15
16
17
18
19
>>> 
```

### Note : when 2 values are given in range function, it starts the range from first to last value.
### If first value is lesser than second, it shows nothing.

3. range(start_val,end_val,step)

Example :
```python
>>> for i in range(10,50,5) : print (i)

10
15
20
25
30
35
40
45
>>> 
```

### Note : step value will be added in each iteeration.
### float values cannot be used in range().

## Set Datatype

Syntax :
```python
set_name={val1,val2...}
```
Example :
```
>>> my_set={1,2,3,4}
>>> type(my_set)
<class 'set'>
>>> 
```
\- Insertion order is not preserved in set.

\- Duplicates are not allowed.

\- Set objects are not subscriptable

Example :
```python
>>> my_set[1]
Traceback (most recent call last):
  File "<pyshell#22>", line 1, in <module>
    my_set[1]
TypeError: 'set' object is not subscriptable
>>> 
```

\- slicing is not allowed

Example :
```python
>>> my_set[1:2]
Traceback (most recent call last):
  File "<pyshell#24>", line 1, in <module>
    my_set[1:2]
TypeError: 'set' object is not subscriptable
>>> 
```

\- Heterogeneous objects are allowed

Example :
```python
>>> my_set={1,2.3,'python',True}
>>> my_set
{2.3, 1, 'python'}
>>> 
```

\- Set is a growable datatype. We can add new elements in set according to need.
Check [Sets in details](src/Chapters/sets_in_detail.md).

## Frozenset Datatype

\- Frozenset is exactly same as set with immutability.

Example :
```python
>>> my_set
{2.3, 1, 'python'}
>>> fs=frozenset(my_set)
>>> fs
frozenset({2.3, 1, 'python'})
>>> fs.add(2)                   # We cannot add or remove elements of frozenset
Traceback (most recent call last):
  File "<pyshell#37>", line 1, in <module>
    fs.add(2)
AttributeError: 'frozenset' object has no attribute 'add'
>>> 
```
Check [frozenset in details](src/Chapters/frozenset_in_detail.md).

## dict Datatype

**Syntax :**
```
dict_name={key:value,key:value}
```

\- Insertion order is preserved in a dictionary.

\- Duplicate keys are not allowed but duplicate values are allowed.

\- Heterogeneous values are allowed.

\- Dictionary is mutable. We can add/remove elements from dictionary.

Example :
```python
>>> my_dict={1:'a',2:'b',3:'c'}
>>> my_dict
{1: 'a', 2: 'b', 3: 'c'}
>>> my_dict[1]
'a'
```
\- check [dictionary](src/Chapters/Dictionaries_in_detail.md) chapter to learn details of dictionaries.

## None datatype

\- None is equivalent to null or void.

\- when a function doesn't return anything, it returns None.

Example :
```python
>>> def my_function():
	a=10

	
>>> print(my_function())
None
>>> 
```
