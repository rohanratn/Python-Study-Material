# Break statement in Python

The break statement terminates the loop containing it. Control of the program flows to the statement immediately after the body of the loop.

If the break statement is inside a nested loop (loop inside another loop), the break statement will terminate the innermost loop.

### Syntax :
```
break
```

### Example :
```python
my_String='Python is an amazing prgramming language'

for letter in my_String :
    if letter == 'a' :
        break
    print(letter, end=' ')
```
### Output :
```
P y t h o n   i s 
```

