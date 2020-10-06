# Tuple in Python

\- tuple is same as list with only different being it is immutable. We cannot change the content of tuple.

\- Insertion order is preserved in tuple.

\- Duplicates are allowed.

\- Heterogeneous elements are allowed.

\- indexing is allowed in tuple.

**Syntax :** 
```
tuple_name=() 
```
Example :
```python
>>> my_tuple=(1,2,3.4,True, 'python')
>>> type(my_tuple)
<class 'tuple'>
>>> my_tuple
(1, 2, 3.4, True, 'python')
>>> 
```
\- A tuple can have list as object and that list is muable.
Example :
```python
>>> my_tuple=(1,2,3,[4,5,6,7])
>>> my_tuple
(1, 2, 3, [4, 5, 6, 7])
>>> my_tuple[3][1]
5
>>> my_tuple[3][1]=8      #  changed the content of list
>>> my_tuple
(1, 2, 3, [4, 8, 6, 7])
>>> 
```
We can perform various operations on/with list datatype.

## Functions of tuple

### 1. count()

\- count method is used to count the number of occurances of passed argument.
```python
>>> my_tuple=(1,1,2,3,4.5, 'Python', 'hello', 'world', 10+3j)
>>> my_tuple
(1, 1, 2, 3, 4.5, 'Python', 'hello', 'world', (10+3j))
>>> my_tuple.count(1)
2
```

### 2. index()
\- index() method returns the index value of passed argument.
```python
>>> my_tuple.index('Python')
5
>>> 
```

### Note : Tuple is an immutable datatype. So we cannot perform operations like lists.