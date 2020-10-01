# Frozenset in Python

\- Frozen set is just an immutable version of a Python set object. While elements of a set can be modified at any time, elements of the frozen set remain the same after creation.

Example :
```
>>> my_set
{2.3, 1, 'python'}
>>> fs=frozenset(my_set)
>>> fs
frozenset({2.3, 1, 'python'})
>>> fs.add(2)                   # We cannot add or remove elements of frozenset
Traceback (most recent call last):
  File "<pyshell#37>", line 1, in <module>
    fs.add(2)
AttributeError: 'frozenset' object has no attribute 'add'
>>> 
```

## Functions of frozenset :

### 1. copy()
\- create a copy of frozenset.

Example :
```
>>> fs2=fs.copy()
>>> fs2
frozenset({1, 2, 3, 4, 5, 6, 7, 8})
>>> 
```

### 2. difference()
\- shows the difference between two or more sets.

```
>>> fs2
frozenset({1, 2, 3, 4, 5, 6, 7, 8})
>>> fs3
frozenset({3, 4, 5, 6, 7, 8})
>>> fs2.difference(fs3)
frozenset({1, 2})
>>> 
```

### 3. intersection()
\- shows the intersection between two or more sets

Example :
```
>>> fs2
frozenset({1, 2, 3, 4, 5, 6, 7, 8})
>>> fs3
frozenset({3, 4, 5, 6, 7, 8})
>>> fs2.intersection(fs3)
frozenset({3, 4, 5, 6, 7, 8})
>>> 
```

### 4. isdisjoint()
\- Returns whether two sets have a intersection or not

Example :
```
>>> fs
frozenset({1, 2, 10, 9})
>>> fs3
frozenset({3, 4, 5, 6, 7, 8})
>>> fs.isdisjoint(fs3)
True
>>> 
```

### 5. issubset()
\- Returns whether another set contains this set or not

Example :
```
>>> fs2
frozenset({1, 2, 3, 4, 5, 6, 7, 8})
>>> fs3
frozenset({3, 4, 5, 6, 7, 8})
>>> fs3.issubset(fs2)
True
>>> 
```

### 6. issuperset()
\- Returns whether this set contains another set or not

Example :
```
>>> fs2
frozenset({1, 2, 3, 4, 5, 6, 7, 8})
>>> fs3
frozenset({3, 4, 5, 6, 7, 8})
>>> fs2.issuperset(fs3)
True
>>> 
```

### 7. symmetric_difference()
\- Returns a set with the symmetric differences of two sets

Example :
```
>>> fs
frozenset({1, 2, 10, 9})
>>> fs2
frozenset({1, 2, 3, 4, 5, 6, 7, 8})
>>> fs.symmetric_difference(fs2)
frozenset({3, 4, 5, 6, 7, 8, 9, 10})
>>> 
```

### 8. union()
\- Return a set containing the union of sets 

Example :
```
>>> fs
frozenset({1, 2, 10, 9})
>>> fs2
frozenset({1, 2, 3, 4, 5, 6, 7, 8})
>>> fs.union(fs2)
frozenset({1, 2, 3, 4, 5, 6, 7, 8, 9, 10})
>>> 
```