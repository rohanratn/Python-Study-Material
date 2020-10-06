## Dictionaries in Python

\- Dictionary datatype is a key-value pair based datatype.

\- for every key, there must be a value specified.

**Syntax :**
```
dict_name={key:value,key:value}
```

\- Insertion order is preserved in a dictionary.

\- Duplicate keys are not allowed but duplicate values are allowed.

\- Heterogeneous values are allowed.

\- Dictionary is mutable. We can add/remove elements from dictionary.

Example :
```python
>>> my_dict={1:'a',2:'b',3:'c'}
>>> my_dict
{1: 'a', 2: 'b', 3: 'c'}
>>> my_dict[1]
'a'
```

## Functions of dictionary

### 1. clear()	
\- Removes all the elements from the dictionary

Example :
```python
>>> my_dict={1:'hello', 2:'world', 3:'python', 4:'programming'}
>>> my_dict
{1: 'hello', 2: 'world', 3: 'python', 4: 'programming'}
>>> my_dict.clear()
>>> my_dict
{}
>>> 
```

### 2. copy()	
\- Returns a copy of the dictionary

Example :
```python
>>> my_dict={1:'hello', 2:'world', 3:'python', 4:'programming'}
>>> my_dict
{1: 'hello', 2: 'world', 3: 'python', 4: 'programming'}
>>> copy_dict=my_dict.copy()
>>> copy_dict
{1: 'hello', 2: 'world', 3: 'python', 4: 'programming'}
>>> 
```

### 3. fromkeys()	
\- Returns a dictionary with the specified keys and value

Example :
```python
>>> keys=(1,2,3,4)
>>> value='a'
>>> my_dict=dict.fromkeys(keys,value)
>>> my_dict
{1: 'a', 2: 'a', 3: 'a', 4: 'a'}
>>> 
```

### 4. get()	
\- Returns the value of the specified key

Example :
```python
>>> my_dict={1:'hello', 2:'world', 3:'python', 4:'programming'}
>>> my_dict.get(2)
'world'
>>> 
```

### 5. items()	
\- Returns a list containing a tuple for each key value pair

Example :
```python
>>> my_dict
{1: 'hello', 2: 'world', 3: 'python', 4: 'programming'}
>>> my_list=my_dict.items()
>>> my_list
dict_items([(1, 'hello'), (2, 'world'), (3, 'python'), (4, 'programming')])
>>> 
```

### 6. keys()	
\- Returns a list containing the dictionary's keys

Example :
```python
>>> my_dict
{1: 'hello', 2: 'world', 3: 'python', 4: 'programming'}
>>> my_list=my_dict.keys()
>>> my_list
dict_keys([1, 2, 3, 4])
>>> 
```

### 7. pop()	
\- Removes the element with the specified key

Example :
```python
>>> my_dict
{1: 'hello', 2: 'world', 3: 'python', 4: 'programming'}
>>> my_dict.pop(2)
'world'
>>> my_dict
{1: 'hello', 3: 'python', 4: 'programming'}
>>> 
```

### 8. popitem()	
\- Removes the last inserted key-value pair

Example :
```python
>>> my_dict
{1: 'hello', 3: 'python', 4: 'programming'}
>>> my_dict.popitem()
(4, 'programming')
>>> my_dict
{1: 'hello', 3: 'python'}
>>> 
```

### 9. setdefault()	
\- Returns the value of the specified key. If the key does not exist: insert the key, with the specified value.

Example :
```python
>>> car = {  "brand": "Ford",  "year": 1964}
>>> x = car.setdefault("model", "Bronco")
>>> print(x)
Bronco
>>> 
```

### 11. update()	
\- Updates the dictionary with the specified key-value pairs.

Example :
```python
>>> car
{'brand': 'Ford', 'year': 1964, 'model': 'Bronco'}
>>> car.update('color':'yellow')
>>> car.update({'color':'yellow'})
>>> car
{'brand': 'Ford', 'year': 1964, 'model': 'Bronco', 'color': 'yellow'}
>>> 
```

### 12. values()	
\- Returns a list of all the values in the dictionary.

Example :
```python
>>> car.values()
dict_values(['Ford', 1964, 'Bronco', 'yellow'])
>>> 
```