# Assignment Operator in Python

\- We can use equals to sign(=) to assign the values to variables.

### Example :
```
>>> x='hello'
>>> y='World'
>>> x
'hello'
>>> y
'World'
>>> 
```

\- If assignment operator is combined with other operators then it is called as compound assignment operator.

### Example : 
```
>>> x=10
>>> y=20
>>> x+=y
>>> x
30
>>> x*=y
>>> x
600
>>> 
```

\- There is no default value provided by python for assignment.

\- Increment and decrement operators are not allowed in python.
### Example :
```
>>> x=10
>>> x++
SyntaxError: invalid syntax
>>> x--
SyntaxError: invalid syntax
>>> 
```

--x or ++x will not give and error. It will simply be treated as -(-x) or +(+x).

### Example :
```
>>> --x
10
>>> ++x
10
```

\- Allowed compound assignment operators

`+=, -=, *=, /=, //=, **=, %=, ^=, &=, |=, >>=, <<=`
