# Exception Handling in Python

Usually there are three types of erros we encounter while running a python program.

1. Compile time error
2. Runtime error
3. Logical error

To handle runtime error, we can use exception handling.

Three keywords are used for exception handling.
### Syntax :
```
try :
    critical-statement
except Exception :
    handle-exception-here
finally :
    default-statements        
```

A critical statement is one which can possibly generate an error. For example a division by zero.

### Example :
```python
val1 = int(input('Enter first number : '))
val2 = int(input('Enter second number : '))

try:
    print(val1 / val2)  # critical statement
except Exception as e:
    print('We\'ve got an error : ', e)
```

### Output 1 :
```
Enter first number : 10
Enter second number : 20
0.5
```
### Output 2 :
```
Enter first number : 12
Enter second number : 0
We've got an error :  division by zero
```

### FInally block is used to perform a default action.
For example we might need to use a resource and we open the resouce but due to an exception it might not get closed. at that time finally block can contain logic to close the resource.

### Example :
```python
val1 = int(input('Enter first number : '))
val2 = int(input('Enter second number : '))

try:
    print('Resource opened')
    print(val1 / val2)  # critical statement
except Exception as e:
    print('We\'ve got an error : ', e)
finally :
    print('Resource closed')

```
### Output 1 :
```
Enter first number : 10
Enter second number : 20
Resource opened
0.5
Resource closed
```

### Output 2 :
```
Enter first number : 10
Enter second number : 0
Resource opened
We've got an error :  division by zero
Resource closed
```

Finally block will execute no matter if there is an exception or not.