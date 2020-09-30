# Python Fundamentals

Following are the basic fundamentals of Python.
*	Indentifiers
*	Reserved words
*	Datatypes
*	Operators

# Indentifiers
A name in python programming language is an Identifier.
for ex. Variables, classes, functions
	
### Rules to declare an Identifier
* An identifier can have only alphabets(upper,lower), Digits(0-9) and Underscore(_)
* Identifier should not start with digits.
* Python is case sesitive language, so CAR != car
* Keywords cannot be used as identifiers
* There is no lenght limit defined to declare an identifier.
* Special symbols are not allowed (!,@,#,$,%,^,&,*,<,>,:,?,/,=,-)
```
>>> 123total					#not allowed
>>> total123					#allowed
>>> java2share					#allowed
>>> ca$h						#not allowed
>>> _abc_abc_					#allowed
>>> def							#not allowed
```		
\- If an identifier start with underscore, it is considered as a private variable.

\- If it starts with 2 underscores, it is considered as strongly private variable.

\- If and identifier starts and ends with 2 underscores, it is language specified variable. e.g. \_\_main\_\_

# Reserved words (keywords)
There are 35 keywords in python.
-	True, False, None	
-	and, or, not, is
-	if, else, elif
-	while, for, break, continue, return, in, yield
-	try, except, finally, raise, assert
-	import, from, as, class, def, pass, global,
	nonlocal, lambda, del, with, async, await
		
## Note : 
\- keywords contain only alphabet symbols.

\- all keywords are in lowercase except True, False , None
			
### To check all keywords,
```
>>> import keyword

>>> keyword.kwlist

['False', 'None', 'True', 'and', 'as', 'assert', 
'async', 'await', 'break', 'class', 'continue', 
'def', 'del', 'elif', 'else', 'except', 'finally', 
'for', 'from', 'global', 'if', 'import', 'in', 
'is', 'lambda', 'nonlocal', 'not', 'or', 
'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
>>>
``` 
# Datatypes

Datatypes represent type of data.

Internally python assigns datatype and user does not need to explicitely specify a datatype.

Type of data | Datatype in Python
----------|----------
Text Type|str
Numeric|int, float, complex
Sequence|list, tuple, range
Mapping|dict
set|set, frozenset
Boolean|bool
Binary|bytes, bytearray, memoryview
Null|None

\- To check a type of object, we can use type() function.

\- We will learn datatypes in detail in [Datatypes](https://github.com/rohanratn/Python-Study-Material/blob/master/Chapters/Datatypes.md) chapter.


# Operators

\- Please click the link to learn about operators in detail

\- Following are categories of operators in Python as follows.

Category|Operator
--------|--------
[Arithmetic](https://github.com/rohanratn/Python-Study-Material/blob/master/Chapters/Arithmetic%20operators.md)| +, -, *, /, %
[Relational/Comparison](https://github.com/rohanratn/Python-Study-Material/blob/master/Chapters/Relational%20operators.md)|>, >=, <, <=, 
[Equality](https://github.com/rohanratn/Python-Study-Material/blob/master/Chapters/Equality%20Operator.md) | ==, !=
[Logical](https://github.com/rohanratn/Python-Study-Material/blob/master/Chapters/Logical%20operator.md)| and, or, not
[Bitwise](https://github.com/rohanratn/Python-Study-Material/blob/master/Chapters/Bitwise%20operators.md)| &, \|, ^, ~, <<, >>
[Assignment](https://github.com/rohanratn/Python-Study-Material/blob/master/Chapters/Assignment%20operator.md) | =
[Special](https://github.com/rohanratn/Python-Study-Material/blob/master/Chapters/Special%20operators.md)| //, **, ternary

