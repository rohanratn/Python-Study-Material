# Command Line arguments

\- Command line arguments are a way to pass input at the time of running the python program.

\- `sys` module needs to be imported in order to use command line arguments.

\- `sys.argv` is a list which contains the passed command line arguments.

\- At the 0'th position of `sys.argv`, filename is stored.

### Example :
To pass command line args
```
py test.py 'hello' 'world' 'python' 'is' 'easy' 123 
```
```python
import sys

#print total number of passed arguments
print(len(sys.argv))

#print filename
print('file name is : ',sys.argv[0])

#print all elements
for i in sys.argv[1:] :
    print(i)

```

### Output
```
PS C:\Users\Rohan\Desktop> py test.py 'hello' 'world' 'python' 'is' 'easy' 123
7
file name is :  test.py
hello
world
python
is
easy
123
PS C:\Users\Rohan\Desktop>
```