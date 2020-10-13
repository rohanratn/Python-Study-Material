# IF statement in python

\- If is a control flow statement which decides which flow to execute based on passed condition.

\- Followong ways we can use `if`statement

## 1. Simple `if` 

### syntax :
```
if <condition> :
    <body of if>
    ------------
    ------------
```

### Example :
```python
my_value=10

if my_value==10 :
    print('Hello world')

```
### Output
```
PS C:\Users\Rohan\Desktop> py test.py
Hello world
PS C:\Users\Rohan\Desktop>
```

if condition is not satisfied, it prints nothing.

## 2. if-else

### Syntax :
```
    if <condition> :
        <body of if>
        -----------
        -----------
    else :
        <body of else>
        -----------
        -----------    
```

### Example :
```python
# Example 1
my_value=10

if my_value==10 :
    print('Hello world')
else :
    print('Value is not 10')

# Example 2    
my_value=20
if my_value==10 :
    print('Hello world')
else :
    print('Value is not 10')

```
### Output :
```
PS C:\Users\Rohan\Desktop> py test.py
Hello world
Value is not 10
PS C:\Users\Rohan\Desktop>
```

## 3. if-else ladder

### Syntax :

```
    if <condition> :
        <body of if>
        -----------
        -----------
    elif <condition> :
        <body of elif>
        -----------
        -----------    
    else :
        <body of else>
        -----------
        -----------
```
### Example :
```python
my_value=int(input('Enter a value : '))

if my_value > 10 :
    print('value is greater than 10')
elif my_value < 10 :
    print('value is lesser than 10')    
else :
    print('value is 10')   
```
### Output :
```
PS C:\Users\Rohan\Desktop> py test.py
Enter a value : 1
value is lesser than 10
PS C:\Users\Rohan\Desktop> py test.py
Enter a value : 20
value is greater than 10
PS C:\Users\Rohan\Desktop> py test.py 
Enter a value : 10
value is 10
PS C:\Users\Rohan\Desktop>
```

### Note : `else` part is always optional.


















