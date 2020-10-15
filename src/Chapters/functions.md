# Functions in Python

We can define a function using `def` keyword.

A function which returns nothing is called as a `void` function.

As a good programming practice, always make a function which returns something.

### Syntax :
```
def function-name(arguments):
    function body
    ------------
    ------------
    return something
```


### Example :
```python
# A function which returns fibonacci series list

def fibonacciList(limit):
    previousNumber,currentNumber = 0,1
    fibonacciList=[]
    while previousNumber <= limit:
        fibonacciList.append(previousNumber)
        previousNumber,currentNumber= currentNumber, currentNumber + previousNumber

    return fibonacciList

# We need to call the function to use it. We can call it simply by its name.
# We also need to catch value returned by the function 
fibonacciList=fibonacciList(300)

# Print the fibonacci series
for i in fibonacciList:
    print(i, end=' ')

```
### Ouput
```
0 1 1 2 3 5 8 13 21 34 55 89 144 233 
```

## Default Argument Values

We can specify default arguments for the function as follows

### Example :
```python
# This function takes `retries` and `reminder` values as default.
# If user wantsdifferent values for it, it can be simply passed in function call

def ask_ok(prompt, retries=3, reminder='Please try again!'):
    while True:
        ok = input(prompt)
        if ok in ('y', 'ye', 'yes'):
            return True
        if ok in ('n', 'no', 'nop', 'nope'):
            return False
        retries = retries - 1
        if retries == 0:
            raise ValueError('invalid user response')
        print(reminder)

try:
    # with default arguments
    ask_ok('Enter a sring : ')

    #with user values
    ask_ok('Enter a sring : ', 2, 'Invalid! Try again.')

except Exception as e :
    print(e)

```

### Output 1 :
```
Enter a sring : w
Please try again!
Enter a sring : w
Please try again!
Enter a sring : w
invalid user response
```

### Output 2 :
```
Enter a sring : w
Invalid! Try again.
Enter a sring : w
invalid user response

```

## Keyword Arguments

We can create functions with keyword arguments as follows.

### Example :
```python
def myFunction(speed,distance='100km', state='Maharashtra'):
    print("Speed is {}. Distance is {}. State is {}".format(speed,distance,state))
```

This function can be called in following ways
```python
myFunction(100)
myFunction(10,'400km')
myFunction(106,'300km','Uttar Pradesh')
myFunction(state='Kashmir', speed='450', distance='200km')

```
### Output :
```
Speed is 100. Distance is 100km. State is Maharashtra
Speed is 10. Distance is 400km. State is Maharashtra
Speed is 106. Distance is 300km. State is Uttar Pradesh
Speed is 450. Distance is 200km. State is Kashmir
```
### Note : if we pass values without using keywords, then it will be assigned as the position in function dfinition.

if we pass keywords with value, the position doesn't matter.


## Functions with variable number of arguments

When we are not sure how many arguments we can pass to a function, we can make it a `var-arg function`

We can pass arguments as follows.

### Example :
```python
def myFunction(*argv):
    for i in argv:
        print(i, end=" ")

myFunction('hahaha','batman','anything', 1,2,3,4)
```

Here `*argv` denotes it is a list containing variable arguments.
We futher can use that list as per need.
### Output :
```
hahaha batman anything 1 2 3 4 
```
## Functions with variable number of keyword arguments

We can define a function to accept keyword. It accepts the input in the format of dictionary as follows.

### Example :
```python
def myFunction(**kwargs):
    print(kwargs.items())
    print(kwargs.keys())
    print(kwargs.values())


myFunction(brand='toyota', color='yellow', type='sedan')
```

### Output :
```
dict_items([('brand', 'toyota'), ('color', 'yellow'), ('type', 'sedan')])
dict_keys(['brand', 'color', 'type'])
dict_values(['toyota', 'yellow', 'sedan'])
```

## Lambda Expressions

Small anonymous functions can be created with the `lambda` keyword.

### Example :
```python

import math

square= lambda x : x ** 2
cube=lambda x : x ** 3
areaOfCircle = lambda x : 2 * math.pi * x

print(square(12))
print(cube(3))
print(areaOfCircle(4))

```
### Output :
```
144
27
25.132741228718345
```