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
```
>>> a=10
>>> b=20
```
### Binary	:
We need to explicitely declare the binary value using \"0b or 0B\"
```
>>>	a=0b1111
>>>	b=0B1111
>>> type(a)
<class 'int'>
```		
Note : When you pass binary to int datatype, it automatically converts binary to int.
```
>>>	a=0b1111
>>> print(a)
15
```
### Octal :
We need to explicitely declare the octal value using \"0o or 0O\".
```
>>>	a=0o1234
>>>	b=-O1234
>>> print(a)
668
```
### Hexadecimal :
We neex to explicitely declare the hexadecimal value using \"0x or 0X\".
```
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
```	
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
```
>>>	f=123.456	# allowed
>>>	f= 0b1111	# not allowed
>>>	f=0xFACE	# not allowed
>>>	f=0o1234	# not allowed
>>> f=123e3		# exponential form is allowed. e3 = 10^3
```				
## Complex Datatype

**format** : a+bj

where,		

	a=real part
	b=imaginary part
	j= underroot -1
Example : 
```
>>>	x=10+2j
>>>	type(x)
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
```
>>> x=10+2j
>>>	x.real
10
>>> x.imag
2.0
```
		
## Boolean Datatype
\- Boolean datatype is used to represent boolean values.

\- Allowed values are True and False (first letter of each is capital).

Example :
```
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
```
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

**syntax :** str[begin:end:step]

Example :
```
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
	
	
	
	
	