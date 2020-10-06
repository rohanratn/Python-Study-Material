# Sets in Python

Syntax :
```
set_name={val1,val2...}
```
Example :
```python
>>> my_set={1,2,3,4}
>>> type(my_set)
<class 'set'>
>>> 
```
\- Insertion order is not preserved in set.

\- Duplicates are not allowed.

\- Set objects are not subscriptable

Example :
```python
>>> my_set[1]
Traceback (most recent call last):
  File "<pyshell#22>", line 1, in <module>
    my_set[1]
TypeError: 'set' object is not subscriptable
>>> 
```

\- slicing is not allowed

Example :
```python
>>> my_set[1:2]
Traceback (most recent call last):
  File "<pyshell#24>", line 1, in <module>
    my_set[1:2]
TypeError: 'set' object is not subscriptable
>>> 
```

\- Heterogeneous objects are allowed

Example :
```python
>>> my_set={1,2.3,'python',True}
>>> my_set
{2.3, 1, 'python'}
>>> 
```

\- Set is a growable datatype. We can add new elements in set according to need.

## Functions of set

### 1. add()	
\- Adds an element to the set

Example :
```python
>>> my_set={1,2,3,4,5}
>>> my_set
{1, 2, 3, 4, 5}
>>> my_set.add(6)
>>> my_set
{1, 2, 3, 4, 5, 6}
>>> 
```

### 2. clear()	
\- Removes all the elements from the set

Example :
```python
>>> copy_set
{1, 2, 3, 4, 5, 6}
>>> copy_set.clear()
>>> copy_set
set()
>>> 
```

### 3. copy()	
\- Returns a copy of the set

Example :
```python
>>> my_set
{1, 2, 3, 4, 5, 6}
>>> copy_set=my_set.copy()
>>> copy_set
{1, 2, 3, 4, 5, 6}
>>> 
```

### 4. difference()	
\- Returns a set containing the difference between two or more sets

Example :
```python
>>> set1
{1, 2, 3, 4, 5, 6}
>>> set2
{1, 2, 3, 5, 6, 7, 9}
>>> set1.difference(set2)
{4}
>>> set2.difference(set1)
{9, 7}
>>> 
```

### 5. difference_update()	
\- Removes the items in this set that are also included in another, specified set

Example :
```python
>>> set1
{1, 2, 3, 4, 5, 6}
>>> set2
{1, 2, 3, 5, 6, 7, 9}
>>> set2.difference_update(set1)
>>> set2
{7, 9}
>>> 
```

### 6. discard()	
\- Remove the specified item

Example :
```python
>>> set1
{1, 2, 3, 4, 5, 6}
>>> set1.remove(4)
>>> set1
{1, 2, 3, 5, 6}
>>> 
```

### 7. intersection()	
\- Returns a set, that is the intersection of two other sets

Example :
```python
>>> set1
{1, 2, 3, 5, 6}
>>> set2
{3, 4, 5, 6, 7, 8}
>>> set1.intersection(set2)
{3, 5, 6}
>>> 
```

### 8.intersection_update()	
\- Removes the items in this set that are not present in other, specified set(s)

Example :
```python
>>> set1
{1, 2, 3, 5, 6}
>>> set2
{3, 4, 5, 6, 7, 8}
>>> set1.intersection_update(set2)
>>> set1
{3, 5, 6}
>>> 
```

### 9. isdisjoint()	
\- Returns whether two sets have a intersection or not

Example :
```python
>>> set1
{1, 2, 3, 4, 5}
>>> set2
{3, 4, 5, 6, 7, 8}
>>> set3
{8, 9, 10, 11, 12, 13}
>>> set1.isdisjoint(set2)
False
>>> set1.isdisjoint(set3)
True
>>> 
```

### 10. issubset()	
\- Returns whether another set contains this set or not

Example :
```python
>>> set1
{1, 2, 3, 4, 5}
>>> set4
{2, 3, 4}
>>> set4.issubset(set1)
True
>>> set1.issubset(set4)
False
>>> 
```

### 11. issuperset()	
\- Returns whether this set contains another set or not

Example :
```python
>>> x = {"f", "e", "d", "c", "b", "a"}
>>> y = {"a", "b", "c"}
>>> z = x.issuperset(y) 
>>> print(z)
True
```

### 12. pop()	
\- Removes an element from the set

Example :
```python
>>> set1
{3, 4, 5, 6, 7, 8}
>>> set1.pop()
3
>>> set1.pop()
4
>>> 
```

### 13. remove()	
\- Removes the specified element

Example :
```python
>>> set1
{5, 6, 7, 8}
>>> set1.remove(6)
>>> set1
{5, 7, 8}
>>> 
```

### 14.symmetric_difference()	
\- Returns a set with the symmetric differences of two sets

Example :
```python
>>> x = {"apple", "banana", "cherry"}
>>> y = {"google", "microsoft", "apple"}
>>> z = x.symmetric_difference(y) 
>>> print(z)
{'banana', 'google', 'microsoft', 'cherry'} 
```

### 15.symmetric_difference_update()	
\- inserts the symmetric differences from this set and another

Example :
```python
>>> x = {"apple", "banana", "cherry"}
>>> y = {"google", "microsoft", "apple"}
>>> x.symmetric_difference_update(y) 
>>> print(x)
{'microsoft', 'cherry', 'banana', 'google'} 
```

### 16. union()	
\- Return a set containing the union of sets

Example :
```python
>>> set1
{1, 2, 5, 7, 8}
>>> set2
{3, 4, 5, 6, 7, 8}
>>> set1.union(set2)
{1, 2, 3, 4, 5, 6, 7, 8}
>>> 
```

### 17. update()	
\- Update the set with the union of this set and others

Example :
```python
>>> set1
{1, 2, 5, 7, 8}
>>> set2
{3, 4, 5, 6, 7, 8}
>>> set1.update(set2)
>>> set1
{1, 2, 3, 4, 5, 6, 7, 8}
>>> 
```

### Note : discard() and remove() methods work exactly same however only difference is, if passed argument is not present in the set, discard() method will not raise an exception but remove() will raise an exception.

Example :
```python
>>> set1
{1, 2, 3, 4, 5, 6, 7, 8}
>>> set1.discard(10)
>>> set1
{1, 2, 3, 4, 5, 6, 7, 8}
>>> set1.remove(10)
Traceback (most recent call last):
  File "<pyshell#229>", line 1, in <module>
    set1.remove(10)
KeyError: 10
>>> 
```