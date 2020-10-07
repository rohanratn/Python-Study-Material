# Type Casting or Type coersion in python

- There are 5 type casting functions available in python.
		
1. int()
2. float()	
3. complex()
4. bool()
5. str()
	
	
## int()
```python
>>>	int(123.456)	#(float to int allowed)
123
>>> int(10+2j)		#(complex to int not allowed)
error
>>>	int(True)		#(bool to int allowed)
1
>>>	int(string)		#(string to int not allowed)
error
>>>	int('10')		#(value as a string allowed)
10
>>>	int("10.2")		#(only int value as a string allowed)
```		
		
## float()
```python		
>>>	float(10)		#(int to float allowed)
10.0
>>>	float(10+2j)	#(complex to float not allowed)
error
>>>	float(True)		#(bool to float allowed)
1.0
>>> float('rohan')	#(string to float not allowed)
error
>>>	float("10.2")	#(value as a string allowed)
10.2
>>> float("0b1111")	#(not allowed)
```		

## complex()
```python
>>> complex(10)		#(int to complex allowed)
10+0j
>>>	complex(10,20)
10+20j
>>>	complex(True)	#(bool to complex allowed)
1+0j
>>> complex(False)
0j
>>> complex("10")	#(value as a string allowed)
10+0j
>>> complex('ten')	#(string to complex not allowed)
```

## bool()
```python		
>>> bool(0)			#(0 is false)
False
>>>	bool(10)		#(non zero is True)
True
>>>	bool(10.20)
True
>>> bool(-10.2)
True
>>> bool(0.0)
False
>>>	bool(10+2j)
True
>>>	bool(0+0j)
False
>>> bool('rohan')
True
>>> bool('')
False
>>> bool(' ')
True
```		

## str()
str() can convert any type to string. There are no restrictions for str.
### Note :  all fundamental datatypes are immutable in python.
```python	
>>> x=10
>>> y=10
>>> id(x)
1234
>>> id(y)
1234
>>> x=20
>>> id(x)
1235				#(new object created)
```
