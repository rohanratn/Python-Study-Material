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

The print() function prints the specified message to the screen, or other standard output device.

The message can be a string, or any other object, the object will be converted into a string before written to the screen.

It has following forms

### Form 1 - print() without arguments.

\- This simply adds a blank line to the terminal

### Example :
```python
>>> print()
                                # blank line
>>> 
```

### Form 2 : print(string)

\- This prints the passed string as output.
\- We can use some operators with print()

### Example :
```python
>>> print('python')
python
>>> print('python'+'world')
pythonworld
>>> print('python'+' '+'world')
python world
>>> print('python' * 2)
pythonpython
>>> print('python','world')
python world
>>> 
```

### Form 3 : print(var-args)

### Example :
```python
>>> a,b,c=10,20,30
>>> print(a,b,c)
10 20 30
>>> 
```

### Note : space is a default separator but we can change the separator useing sep parameter.

### Example 
```python
>>> print(a,b,c, sep='*')
10*20*30
>>> print(a,b,c, sep='\n')
10
20
30
>>> print(a,b,c, sep='\t')
10	20	30
>>> print(a,b,c, sep='\r')
10
20
30
>>> print(a,b,c, sep='\b')
102030
>>> print(a,b,c, sep='-')
10-20-30
>>> print(a,b,c, sep=':')
10:20:30
>>> 
```

### Form 4 : print(`end`)
\- This parameter specified the end of the ouput.

### Example :
```python
>>> print('hello', end='\n')
hello
>>> print('hello', end='-')
hello-
>>> print('hello', end=':')
hello:
>>> print('hello', end='\t')
hello	
>>> 
```
By default value for `end` parameter is a newline character.

### Form 5: print(formatted string)

### Example :
```python
>>> a=10
>>> b=20
>>> print("a value is %i"%a)
a value is 10
>>> print("b value is %i"%b)
b value is 20
>>> print("a and b are %i and %i"%(a,b))
a and b are 10 and 20
>>> 
>>> a=10.34
>>> print("a value is %f"%a)
a value is 10.340000
>>> 
```

### Form 6 : print() with replacement operator

`{ }` is replacement operator for pprint().

### Example :
```python
>>> name='xyz'
>>> salary = 123456
>>> print('name is {name} and salary is {salary}'.format(name,salary))
Traceback (most recent call last):
  File "<pyshell#36>", line 1, in <module>
    print('name is {name} and salary is {salary}'.format(name,salary))
KeyError: 'name'
>>> print('name is {0} and salary is {1}'.format(name,salary))
name is xyz and salary is 123456
>>> print('name is {x} and salary is {y}'.format(name,salary))
Traceback (most recent call last):
  File "<pyshell#38>", line 1, in <module>
    print('name is {x} and salary is {y}'.format(name,salary))
KeyError: 'x'
>>> print('name is {x} and salary is {y}'.format(x=name,y=salary))
name is xyz and salary is 123456
>>> print('name is {x} and salary is {y}'.format(x=name,y=salary))
name is xyz and salary is 123456
>>> 
```

Check [Python print format](https://www.w3schools.com/python/ref_string_format.asp) for more information.


