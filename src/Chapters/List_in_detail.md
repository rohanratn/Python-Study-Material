# Lists in Python

\- we can store heterogeneous data elements in a single list

\- Insertion order is preserved and duplicates are allowed in list.

\- List is a mutable datatype. We can change the contents of list.

Syntax :
```
>>> list_name=[element1, element 2......]
```
### Note : items in list are separated by comma.

Example :
```python
>>> my_list=[1,2,3.4,10+20j]
>>> my_list=[1,2,3.4,10+20j, 'Python']		# Heterogeneous elements
>>> type(my_list)
<class 'list'>
>>> for i in my_list: print(i)

1
2
3.4
(10+20j)
Python
>>> 
```

\- First element is present at list[0] position and last is present at list[-1]

\- List supports negative indexing

## Functions of list

Following are functions provided for list operations

### 1. append() 
\- append() method adds an element at the end of the list.

Example :
```python
>>> my_list=[1,2,3,4]
>>> my_list
[1, 2, 3, 4]
>>> my_list.append(5)
>>> my_list
[1, 2, 3, 4, 5]
>>> my_list.append(8)
>>> my_list
[1, 2, 3, 4, 5, 8]
>>> 
```

### 2. extend(iterable)
\- extend() method allowes user to add multiple elements at the end of the list. in other words, it can be used to join two or more lists.

Example :
```python
>>> my_list
[1, 2, 3, 4, 5, 8]
>>> my_list.extend(['hello','world'])
>>> my_list
[1, 2, 3, 4, 5, 8, 'hello', 'world']
>>> 
```

### 3. insert(i, x)
\- insert()method is used to insert an element at given position.

\- first argument is the position and second argument is value.

Example :
```python
>>> my_list
[1, 2, 3, 4, 5, 8, 'hello', 'world']
>>> my_list.insert(2,"python")
>>> my_list
[1, 2, 'python', 3, 4, 5, 8, 'hello', 'world']
>>> 
```

### 4. remove(x)
\- Removes the first item from the list that has a value of x. Returns an error if there is no such item.

Example :
```python
>>> my_list
[1, 2, 'python', 3, 4, 5, 8, 'hello', 'world']
>>> my_list.remove(3)
>>> my_list
[1, 2, 'python', 4, 5, 8, 'hello', 'world']
>>> 
```

### 5. pop(i)
\- Removes the item at the given position in the list, and returns it. If no index is specified, pop() removes and returns the last item in the list.
```python
>>> my_list
[1, 2, 'python', 4, 5, 8, 'hello', 'world']
>>> my_list.pop(2)
'python'
>>> my_list
[1, 2, 4, 5, 8, 'hello', 'world']
>>> my_list.pop()
'world'
>>> my_list
[1, 2, 4, 5, 8, 'hello']
>>> 
```

### 6. clear()
\- Removes all items from the list. Equivalent to del a[:].

Example :
```python
>>> my_list
[1, 2, 4, 5, 8, 'hello']
>>> my_list.clear()
>>> my_list
[]
>>> 
```

### 7. index(x)
\- Returns the position of the first list item that has a value of x. Raises a ValueError if there is no such item.

Example :
```python
>>> my_list
[1, 2, 3, 4, 5, 6, 7, 8, 'python', 'hello', 'world']
>>> my_list.index('python')
8
>>> 
```

### 8. count(x)
\- Returns the number of times x appears in the list.

Example :
```python
>>> my_list
[1, 2, 3, 4, 5, 6, 7, 8, 'python', 'hello', 'world', 2, 3, 2, 4, 2]
>>> my_list.count(2)
4
>>> 
```

### 9. sort(key=None, reverse=False)

\- Sorts the items of the list in place. The arguments can be used to customize the operation.

\- key
```
Specifies a function of one argument that is used to extract a comparison key from each list element. 
The default value is None (compares the elements directly.
```
\- reverse
```
Boolean value. If set to True, then the list elements are sorted as if each comparison were reversed. 
```

Example 1 :
```python
>>> my_list=[6,3,5,2,7,1,4]
>>> my_list
[6, 3, 5, 2, 7, 1, 4]
>>> my_list.sort()
>>> my_list
[1, 2, 3, 4, 5, 6, 7]
>>> my_list.sort(reverse=True)
>>> my_list
[7, 6, 5, 4, 3, 2, 1]
```

Example 2 :
```python
>>> my_list=['Python','hello','transformers', 'bee']
>>> my_list
['Python', 'hello', 'transformers', 'bee']
>>> my_list.sort(key=len)
>>> my_list
['bee', 'hello', 'Python', 'transformers']
```

### 10. reverse()
\- It reverses the list.

Example :
```python
>>> my_list
[1, 2, 3, 4, 5, 6, 7, 8]
>>> my_list.reverse()
>>> my_list
[8, 7, 6, 5, 4, 3, 2, 1]
>>> 
```

### 11. copy()

\- Returns a shallow copy of the list

Example :
```python
>>> copy_list=my_list.copy()
>>> copy_list
[8, 7, 6, 5, 4, 3, 2, 1]
>>> 
```
