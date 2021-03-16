## What is Python

- Python is a free, open-source, object-oriented programming language

    - Stong community support
    - 1000s packages you may download and reference (language processing, facial recongition etc.)
    
    Examples:<br>
    - scipy, numpy, pandas, mpi4py for science
    - pyQT for GUI interface devlopment
    - APIs - LinkedIn, CraigsList, Google, BeautifulSoup
    - TensorFlow for Machine Learning
    - nltk for Natural Lanaguage Processing and Analysis
    - py2FaceR for Facial Recognition
    <br>
<br>
    
- Objects can have properties and methods:
    - Properties – Name, Spatial Reference, Extent, etc. 
    - Method – Something the object can do
<br>
<br>
- Scripting allows you to automate time-consuming and complex process so you can work more efficiently.


## How do I get it

#### Python 

Python of "free" but is curated by several organizations (some for profit)

https://anaconda.org/<br>
https://www.enthought.com/product/canopy/<br>
https://www.python.org/

#### PyPI - the Python Package Index

The Python Package Index is a repository of software for the Python programming language. Currently the repository contains over 130,000 packages. 

https://pypi.python.org/pypi


#### Make No Commitments

http://pythonfiddle.com/

## Some Python Miscellany

- Python is interpreted
- Python is case-sensitive
- Python uses indentation to define code blocks
- '#' is used to designate comment code (and '"""' ...'"""' for multi-line comments)
- '\*' is a wildcard character in strings (useful for finding or identifying specific files: “I:\plays\\\*henry\*.doc”)
- = vs ==
    - = is used for assignment.
    - == is used to test for equivalency


## Data Types
- Numbers 
    - Integer/Long Integer, Float
- Strings
    - Text 
- Lists
    - Ordered list of numbers, strings, other lists, or combinations of data types.
- Dictionaries
    - Keyed collection of numbers, strings, other lists, or combinations of data types.
- Tuples
    - Similar to list above but immutable (useful for indexing)

## Numbers
- Assign number values to variables using =
- Convert between integer and floating point using int() and float() functions.
- Numbers can be converted into strings using the str() function
- Python cannot concatenate numbers and strings



```python
number = 14
print(number)
```

    14
    


```python
float(number)
```




    14.0




```python
int(number)
```




    14




```python
str(number)
```




    '14'




```python
year = 2018
s = "number = {0}".format(year)
print(s)

print(f'number = {year}')
```

    number = 2018
    number = 2018
    

<table style="width:100%">
<tr>
    <th><p align="left">Op</p></th>
    <th><p align="left">Arithmetic Operators</p></th>
    <th><p align="left">Op</p></th>
    <th><p align="left">Comparison Operators</p></th>
</tr>
<tr>
    <td><p align="left">+ </p></td>
    <td><p align="left">Addition            </p></td>
    <td><p align="left">==    </p></td>
    <td><p align="left">Is Equal To             </p></td>
</tr>
<tr>
    <td><p align="left">- </p></td>
    <td><p align="left">Subtraction         </p></td>
    <td><p align="left">!=    </p></td>
    <td><p align="left">Does Not Equal          </p></td>
</tr>
<tr>
    <td><p align="left">&#42; </p></td>
    <td><p align="left">Multiplication      </p></td>
    <td><p align="left">&lt;&gt;</p></td>
    <td><p align="left">Does Not Equal          </p></td>
</tr>
<tr>
    <td><p align="left">/ </p></td>
    <td><p align="left">Division            </p></td>
    <td><p align="left">&gt;  </p></td>
    <td><p align="left">Greater Than            </p></td>
</tr>
<tr>
    <td><p align="left">% </p></td>
    <td><p align="left">Modulus             </p></td>
    <td><p align="left">&lt;  </p></td>
    <td><p align="left">Less Than               </p></td>
</tr>
<tr>
    <td><p align="left">&#42;&#42;</p></td>
    <td><p align="left">Exponent            </p></td>
    <td><p align="left">&gt;= </p></td>
    <td><p align="left">Greater Than or Equal To</p></td>
</tr>
<tr>
    <td><p align="left">//</p></td>
    <td><p align="left">Floor Division      </p></td>
    <td><p align="left">&lt;= </p></td>
    <td><p align="left">Less Than or Equal To   </p></td>
</tr>
</table>

## Strings
- Strings are defined by single or double quotes ("Hello World")
- Strings are a collection of characters
- Individial characters may be accessed via and index
- Backslashes are escape characters in Python. Use 'r' (raw) to define strings that contain backslashes
- Strings are concatenated using the '+' operator


```python
example = "Hi"
example = 'Hello world'
print(example)
```

    Hello world
    


```python
print(example[0])
print(example[1])
print(example[2])
print(example[3])
print(example[4])
```

    H
    e
    l
    l
    o
    


```python
filePath = "C:\\users\\chuck\\Tools"
print(filePath)
filePath = r"C:\users\chuck\Tools"
print(filePath)
```

    C:\users\chuck\Tools
    C:\users\chuck\Tools
    


```python
example = "Hi " + "everyone"
print(example)
```

    Hi everyone
    

<table style="width:100%">
<tr>
    <th><p align="left">String Method</p></th>
    <th><p align="left">Description</p></th>
    <th><p align="left">Examples: <br> &gt;&gt;&gt; txt = r“I:\GIS\clayton.shp”</p></th>
</tr>

<tr>
<td><p align="left">.startswith(prefix)</p></td>
<td><p align="left">Returns True if string starts with prefix.</p></td>
<td><p align="left"> &gt;&gt;&gt; txt.startswith(“I:\GIS”)<br>True</p></td>
</tr>

<tr>
<td><p align="left">.endswith(suffix)</p></td>
<td><p align="left">Returns True if string ends with suffix. <br>*Useful for finding filetypes!</p></td>
<td><p align="left"> &gt;&gt;&gt; txt.endswith(“.shp”)<br>True</p></td>
</tr>

<tr>
<td><p align="left">.isalnum(string)</p></td>
<td><p align="left">Returns True if all characters in string are <br>alphanumeric.</p></td>
<td><p align="left"> &gt;&gt;&gt; txt.isalnum()<br>False</p></td>
</tr>

<tr>
<td><p align="left">.replace(old, new)</p></td>
<td><p align="left">Returns a copy of the string with <br>all occurrences of old replaced <br>by new.</p></td>
<td><p align="left"> &gt;&gt;&gt; txt.replace(“GIS”, “GDB”)<br>"I:\\GDB\\clayton.shp"</p></td>
</tr>

<tr>
<td><p align="left">.split(sep)</p></td>
<td><p align="left">Returns a list of the words in a string, using sep <br>as the delimiter.</p></td>
<td><p align="left"> &gt;&gt;&gt; txt.split(“\\”)<br>["I:" , "GIS" , "clayton.shp"]</p></td>
</tr>

<tr>
<td><p align="left">.strip(chars)</p></td>
<td><p align="left">Returns a copy of the string with the leading/<br>trailing chars removed. If no chars given, <br>whitespace is removed.</p></td>
<td><p align="left"> &gt;&gt;&gt; txt.strip(“.shp”)<br>"I:\\GIS\\clayton"</p></td>
</tr>

</table>

## Lists

- Lists are ordered sets of data elements enclosed in square brackets
- Items in lists are ordered 0, 1, 2, 3, etc. 
- Items in the list may be of different types
- To retrieve a specific item, give the list name followed by the item’s index (i.e.,order) number enclosed in square brackets
- List comprehensions are a special construct for the creation of lists


```python
emptyList = []
Cities = ["Houston" , "Austin" , "Dallas"]
print(Cities)
print(Cities[0])
print(Cities[1])
print(Cities[2])
```

    ['Houston', 'Austin', 'Dallas']
    Houston
    Austin
    Dallas
    


```python
list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print(list)
list = [x for x in list if (x % 2) == 0 ]
print(list)
```

    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    [0, 2, 4, 6, 8]
    

<table style="width:100%">
<tr>
    <th><p align="left">List Method</p></th>
    <th><p align="left">Description</p></th>
    <th><p align="left">Examples: <br> &gt;&gt;&gt; list = ['a', 'd', 'c', 'b']</p></th>
</tr>

<tr>
<td><p align="left">.append(item)</p></td>
<td><p align="left">Add item to the list.</p></td>
<td><p align="left"> &gt;&gt;&gt; list.append(‘e’)<br>['a', 'd', 'c', 'b', 'e']</p></td>
</tr>

<tr>
<td><p align="left">.sort()</p></td>
<td><p align="left">Sort the items of a list.</p></td>
<td><p align="left"> &gt;&gt;&gt; print list.sort()<br>['a', 'd', 'c', 'b']</p></td>
</tr>

<tr>
<td><p align="left">.reverse()</p></td>
<td><p align="left">Reverse the item order.</p></td>
<td><p align="left"> &gt;&gt;&gt; print list.reverse()<br>['b', 'c', 'd', 'a']</p></td>
</tr>

<tr>
<td><p align="left">.remove(x)</p></td>
<td><p align="left">Remove the first item from the list whose value is x.</p></td>
<td><p align="left"> &gt;&gt;&gt; print list.remove('a')<br>['d', 'c', 'b']</p></td>
</tr>

<tr>
<td><p align="left">.insert(#, item)</p></td>
<td><p align="left">Insert item into the list at the list position #.</p></td>
<td><p align="left"> &gt;&gt;&gt; print list.insert(0,'z')<br>['z', 'a', 'd', 'c', 'b']</p></td>
</tr>

<tr>
<td><p align="left">.count(x)</p></td>
<td><p align="left">Count the number of times x appears in the list.</p></td>
<td><p align="left"> &gt;&gt;&gt; print list.count('c')<br>1</p></td>
</tr>

</table>

## Dictionaries
- Dictionaries are unordered sets of key value pairs enclosed in curley brackets
- Items in the dictionary may be of different types
- To retrieve a specific item, give the dictionary name followed by the item’s key enclosed in square brackets
- Dictionary comprehensions are a special construct for the creation of dictionaries



```python
emptyDictionary = {}
emptyDictionary["cat"] = 1
emptyDictionary["dog"] = "happy"
print("emptyDictionary[\"cat\"] = {0}".format(emptyDictionary["cat"]))
print("emptyDictionary[\"dog\"] = {0}".format(emptyDictionary["dog"]))
```

    emptyDictionary["cat"] = 1
    emptyDictionary["dog"] = happy
    


```python
CityPopulations = { "Houston":2000000 , "Austin":1500001 , "Dallas":3000000 }
print(CityPopulations)
print(CityPopulations["Austin"])
```

    {'Houston': 2000000, 'Austin': 1500001, 'Dallas': 3000000}
    1500001
    


```python
CityPopulations = {k:v for (k,v) in CityPopulations.items() if (v % 2) == 0}
print(CityPopulations)
```

    {'Houston': 2000000, 'Dallas': 3000000}
    


```python
CityPopulations.items()

```




    dict_items([('Houston', 2000000), ('Dallas', 3000000)])



<table style="width:100%">
<tr>
    <th><p align="left">Dictionary Method</p></th>
    <th><p align="left">Description</p></th>
    <th><p align="left">Examples: <br> &gt;&gt;&gt; dict = {'a':0, 'd':1}</p></th>
</tr>

<tr>
<td><p align="left">.items()</p></td>
<td><p align="left">Returns a view of the dictionary's (key,value) pairs.</p></td>
<td><p align="left"> &gt;&gt;&gt; dict.items(‘e’)<br>dict_items([('a':0), ('d':1)])</p></td>
</tr>

<tr>
<td><p align="left">.keys()</p></td>
<td><p align="left">Returns a view object of all keys.</p></td>
<td><p align="left"> &gt;&gt;&gt; print dict.keys()<br>dict_keys(['a', 'd'])</p></td>
</tr>

<tr>
<td><p align="left">.values()</p></td>
<td><p align="left">Returns a view object of all values.</p></td>
<td><p align="left"> &gt;&gt;&gt; print dict.values()<br>dict_values([0, 1])</p></td>
</tr>

<tr>
<td><p align="left">.pop(key)</p></td>
<td><p align="left">Returns an item and deletes it from the dictionary.</p></td>
<td><p align="left"> &gt;&gt;&gt; print dict.pop('a')<br>{'d':1}</p></td>
</tr>

<tr>
<td><p align="left">.clear()</p></td>
<td><p align="left">Removes all items from the dictionary.</p></td>
<td><p align="left"> &gt;&gt;&gt; print dict.clear()<br>{}</p></td>
</tr>

</table>

## Tuples
- Tuples are ordered sets of data elements enclosed in parenthesis
- Tuples are very similar to lists
- Tuples are immutable and therefore are useful as indexers


```python
person = ("Chuck", "Knight")
print(person[0])
```

    Chuck
    


```python
people = {}
people[("Chuck", "Knight")] = 10
people[("Kody", "Knight")] = 11
people[("William", "Tell")] = 0
print(people)
```

    {('Chuck', 'Knight'): 10, ('Kody', 'Knight'): 11, ('William', 'Tell'): 0}
    


```python
person = ("Chuck", "Knight")
person[0] = "not chuck"
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-36-cf59a9b45c74> in <module>
          1 person = ("Chuck", "Knight")
    ----> 2 person[0] = "not chuck"
    

    TypeError: 'tuple' object does not support item assignment


## Conditions and Loops
- All conditional and loop statements end with a ':'
- Code within a conditional or loop is nested using spaces

## if - elif - else Statements
- Perform some operation if a statement is true otherwise (else) do something else
- Boolean operators were listed previously (under Numbers)


```python
pi = 1.14
if pi >= 4:
    print("pi is greater than or equal to 4")
elif pi > 3:
    print("pi is greater than or equal to 3 but less than 4")
else:
    print("pi is not greater than or equal to 3")
    
```

    pi is not greater than or equal to 3
    


```python
pi = 3.14
if pi >= 4:
    print("pi is greater than or equal to 4")
else:
    if pi > 3:
        print("pi is greater than or equal to 3 but less than 4")
    else:
        print("pi is not greater than or equal to 3")
```

    pi is greater than or equal to 3 but less than 4
    

## for - else Statements
- Loops are used to iterate over a collection/range of elements
- Like other languages Python has the concept of break and continue for loops
- Unlike other languages a for loop may have an else clause
- Introducing range() - used to create iteration indices


```python
list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
for x in list:
    print(x)
```

    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    


```python
for x in range(0, 10):
    print(x)
```

    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    


```python
list = []
for x in list:
    print(x)
else:
    print("There were no elements")
```

    There were no elements
    

## while - else Statements
- Loops are used to iterate some criteria are met (some statement is true)
- Again
    - Like other languages Python has the concept of break and continue for loops
    - Unlike other languages a while loop may have an else clause
- Introducing pass - The no op command



```python
count = 0
while (count < 9):
   print("The count is: {0}".format(count))
   count = count + 1
```

    The count is: 0
    The count is: 1
    The count is: 2
    The count is: 3
    The count is: 4
    The count is: 5
    The count is: 6
    The count is: 7
    The count is: 8
    


```python
# The else clause acts like the finally statment in other languages 
# (always executed once at the end of any iterations)
count = 5
while (count < 9):
   print("The count is: {0}".format(count))
   count = count + 1
else:
    print("count was never less than 9")
```

    The count is: 5
    The count is: 6
    The count is: 7
    The count is: 8
    count was never less than 9
    


```python
count = 10
while (count < 9):
   print("The count is: {0}".format(count))
   count = count + 1
else:
    print("count was never less than 9")
```

    count was never less than 9
    


```python
# Using the pass statment (a no op) until a decision structure can be defined later
count = 10
while (count < 9):
    pass
```

## Modules
- At some point you will want to use other peoples Python code
- Importing allows your Python code to see installed Python packages
- You can use OPPC either from it's native namespace or merge it into yours 

Some core modules
- os – Operating system functions
- sys – System-specific parameters and functions
- glob – Unix-style pathname patterns
- csv – CSV file reading and writing


```python
# How to tell what version of a package we are using
import sys
print(sys.version)
```

    3.7.6 (default, Jan  8 2020, 20:23:39) [MSC v.1916 64 bit (AMD64)]
    


```python
# A simple import which requires a namespace prefix to use its methods
import os as o
print(o.getcwd())
```

    C:\Users\caknigh\LocalData\DevArea\projects\Trenton-Computer-Festival
    


```python
# Merge a single import into our namespace (so that no qualifier needed)
from time import sleep
print("Sleeping...")
sleep(1)
print("done!")
```

    Sleeping...
    done!
    


```python
# Merge all imports into our namespace (so that no qualifiers are needed)
# Other than those prefixed by "_" which implements a crude form of encapsulation
from random import *
print("randint = {0}".format(randint(0, 10)))
```

    randint = 0
    


```python

```
