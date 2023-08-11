# Section Introduction
We will learn:
- Operators supported by strings
- String methods

# Introduction to String
Indexing:
|H|e|l|l|o|
|-|-|-|-|-|
|0|1|2|3|4|
|-5|-4|-3|-2|-1|

Any string is object of `str` class.  

Methods:
input()  
len() - gives us length of a string, i.e. the number of characters in a string.  

We can traverse a string using for loop.
```python
for x in s1:
    statement 1
```

To write a string in multiple lines, use triple (`'''` or `"""`) quotes.  

# Operators on Strings
Operators that work on strings:
1. Concatenation
1. Repetition
1. Indexing
1. Slicing
1. in
1. not in

### Concatenation
Method 1:
```python
s1 = 'Hello'
s2 = 'world'
s3 = s1 + s2
# s3 becomes 'Helloworld'
```

It will create a new object and s3 will point to that in memory.  

Method 2:
```python
s4 = 'Hello' 'world'
s4 = s1 s2 # This will give error. Space doesn't work with variables only with literals.
# s4 becomes 'Helloworld'
```

**Note:** `,` will not combine them. That only works in `print()` function.  

Method 3:
```python
# Only strings can be combined together
s5 = 'Hello' + 15 # This will give error
s6 = 'Hello' + str(15) # str() method converts 15 to a str object. Then concatenation happens.
```

### Repetition
```python
s1 = 'Hi'
s2 = s1 * 3 # Multiplication can only happen with integer.
# s2 becomes 'HiHiHi'.
```

### Indexing
```python
s1 = 'Hello world'
s2 = s1[4] # s2 becomes 'o'
```

### Slicing
```python
s1 = 'Hello world'
s2 = s1[start: end: step]
```

**Note:** Slicing gives a separate string.

### in and not-in
```python
s1 = 'Hello world'
'H' in s1 # gives True
'wo' in s1 # True
'me' not in s1 # True
# We can check for substrings also.
```

# Relational Operators on Strings
Operators are:
- <
- <=
- \>
- \>=
- ==
- !=

We have already seen how these work.  
They compare the unicode values character by character.

# Introduction to String Methods
Class will contain:
- Data
- Operations/functions

len() is a function.  
If a function is present inside a class, then we call them methods.  

`str` class has a lot of methods built inside it.  

```python
s = "My string"
type(s)
# Gives -> <class 'str'>
# To see the definition of any class
dir(str)
# This shows all the methods available in the class.
```

dir() function returns all properties and methods of the specified object, without the values.  

We can also give an object of a particular class inside the `dir()` function.  

To know what a particular method do use `help() method`.  
For that we need to first have an object of the class.  

`help(s.endswith)`

## String Methods: find() and index()
Methods:
- find()
- rfind() - reverse find
- index()
- rindex() - reverse index
- count()


**`find()`** - finds the existence of a given substring.  
`string.find('substring')`  
Returns the starting index of the substring. If not found it will returns -1.  
This will start looking from the first index.  
The general usage is: `s.find(substring, start, end)`.  
```python
s = 'hello, how are you'
s.find('o') # Gives 4
s.find('o', 5) # Gives 8
s.find('o', 5, 8) # Gives -1. It does not include the end index
```

**Note:** General Notation: `S.find(sub[, start[, end]])`. Here [] denote optional inputs.  

**`rfind()`** - does the same thing as find(), but starts searching from the end.  
Returns the index, and -1 if not substring is not there.
```python
s.rfind('o') # Gives 16
s.rfind('o', 0, 15) # Gives 8
# It starts from the end, but the indices are given in the forward direction only.
```

**`index()`** - same as find() except that it gives an error when the substring is not found.  
General syntax: `S.index(sub[, start[, end]])`  
The case of **`rindex()`** is similar to rfind().

**`count()`** - counts the total occurrences of a substring.  
General syntax: `S.count(sub[, start[, end]])`.

## String Methods: Removing Spaces
Alignment methods:
- ljust(width [, fill])
- rjust(width [, fill])
- center(width [, fill])

These are useful when we want to write a string in extra spaces with some particular alignment.  
`width` - specifies the total spaces in which to do the alignment. If the width specified is smaller than the total length then no alignment happens.  
`fill` - s.center(10, '*') will fill the empty spaces with *'s. This is optional parameter.  
Note: These methods create a new string, and do not affect the original ones.

```python
s = 'python'
s1 = s.ljust(10) # Generates 'python1234' where numbers denote spaces.
s2 = s.center(20, '+')
```

Space/character removal methods:
- strip([chars])
- lstrip([chars]) - remove leading characters
- rstrip([chars]) - remove trailing characters

Without any input they remove the spaces. If we specify the character then that particular character's occurrences are removed. Do not affect the original string.  
```python
s = '...   ...   +++ aapython'
s.lstrip() # Nothing happens as no leading spaces.
s.lstrip('.') # Removes all the leading dots until the first space.
s.strip('. +a') # Removes ., space, +, a all of them.
# The above generates 'python'
```

## String Methods: Changing Cases
Methods:
- capitalize() - capitalizes the first letter, everything else is made lower case.
- lower()
- upper()
- title()
- swapcase() - Every word's first letter is made capital, everything else is made lower case.
- casefold() - converts to lower case. Many languages have upper and lower cases. some characters don't have lower case, they are caseless. For these characters, lower() doesn't do anything, but casefold() converts them to some equivalent lower case.

> [!NOTE]
> These all generate new strings, the original string is not modified. As string is immutable.

**Note:** To write unicode characters in string use: `s1 = 'Bu\u00DF'`.

## String Methods: Inquiry Methods
All these method names start with 'is'. All of them return boolean values.  

- **isupper()** - returns True if all characters are in upper case.
- **islower()**
- **istitle()**

If the string is empty then they return False.  
If the string contains numbers also then they are ignored.  

- **isalnum()** - if a string only contains alphabets and numbers then it returns True. Will return False if there are special symbols or is empty.
- **isalpha()** - if a string contains only alphabets then it returns True.
- **isspace()** - checks if a string contains only spaces then it returns True.
- **isascii()** - returns True if string only contains ASCII characters. Returns True even if empty.

- **isidentifier()** - returns True if the string is a valid variable(identifier) name.
- **isprintable()** - some special characters such as \n, \t, \r are not printable. If a string only contains printable characters then it returns True.

- **isdecimal()** - returns True if a string contains only integer numbers.
- **isdigit()** - if numbers are in special form, even then it will return True. Eg: in superscript.
- **isnumeric()** - Eg: 5 raised to 1/2.

## String Methods - Starts with and Ends with
Methods:
- startswith(prefix [, start[, end]])
- endswith(suffix [, start[, end]])
- removesuffix(suffix, /)
- removeprefix(prefix, /)
- partition(sep)
- rpartition(sep)

**startswith()** - checks if a particular string starts with given substring or not.  
**removesuffix()** - removes the given substring from a given string if present, otherwise original string is returned.  
Eg: can be used with email IDs. To check if a particular email id is from gmail, or for removing the end and retain only username.  
**partition()** - breaks a string into 3 parts not containing the given substring, which is removed. It returns a tuple of 3 strings.  
```python
s = 'python is very easy'
s.partition('is')
t = ('python ', 'is', ' very easy')
```
rpartition() - does the same thing but from the end. That is partitions into 3 starting from the first occurrence from the right.

## String Methods - Joining and Splitting
Methods:
- replace(old, new[, count])
- join(iterable)
- split([sep[, max split]])
- rsplit([sep [, max split]])
- splitlines([keepends])

Details:  
**replace(old, new[, count])** - replaces given substring with another.  
The optional count parameter allows us to determine how many of the old substring we want to replace.  
If the given substring is not present then the original string is returned.
```python
s = 'a-b-c-d-e'
s.replace('-', ',')
# Generates new modified string 'a,b,c,d,e'
s.replace('-', ',')
# Generates 'a,b,c,d-e'
```

**join(iterable)** - goes over the specified substring and adds given string in between as a separator concatenator.
```python
s1 = 'xyz'
s2 = 'abc'
s1.join(s2) # Generates 'axyzbxyzc'
# Adds s1 only in between not in the beginning or at the end. It acts like a separator.
s1 = '/'
s2 = 'abc'
s1.join(s2) # Generates 'a/b/c'
# Parts of s2 are joined together using s1 as the separator
```

Now for iterable:
```python
l1 = ['john', 'smith', 'ajay']
s1 = ','
s1.join(l1)
# Generates 'john,smith,ajay'
```

**split([sep[, max split]])** - Explained by example.
```python
s = 'john smith ajay'
s.split() # Generates the list ['john', 'smith', 'ajay']
s = 'john,smith,ajay'
s.split(',') # Generates ['john', 'smith', 'ajay']
s.split(',', 1) # Generates ['john', 'smith,ajay']
```

**rsplit([sep [, max split]])** - starts splitting from the end. So the effect of count is different as it begins from the end.  

**splitlines([keepends])** - similar to split() but this works by default on ['\n', '\r', '\f'] whereas split() by default works with ' '.  
if keepends parameter is set to True, then it will keep the newline characters also in the splitted strings.
```python
s = 'aaa\nbbb\tccc\rddd\feee'
s.splitlines() # Generates ['aaa', 'bbb\tccc', 'ddd', 'eee']
s.splitlines(keepends = True) # Generates ['aaa\n', 'bbb\tccc\r', 'ddd\x0c', 'eee']
# Difference with split()
s.split() # Generates ['aaa', 'bbb', 'ccc', 'ddd', 'eee']
# split() works with tabs and new lines characters also.
```