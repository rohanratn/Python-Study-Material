# Continue statement in Python

The continue statement **skips the code that comes after it**, and the control is passed back to the start for the next iteration.

### Syntax :
```
continue
```

### Example :
```python
myNumbers=[1,2,3,4,5,6,7,8,9,10]

for numbers in myNumbers :
    if numbers == 4 or numbers == 7 :
        continue
    print(numbers, end=' ')
```
### Output 
```
1 2 3 5 6 8 9 10 
```








