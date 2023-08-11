# Contents
There are lot of datatypes in python.
We will learn basics of all and in detail we will study:
Numeric Types

We will also learn about concepts related to datatypes:
Variables
Literals
Conversions


# What are Variables?
Important elements of a program are:
1. Data
2. Instructions - work on the data

Variable is reference to data.

Whenever we declare a variable in python, we also initialize it.
a = 10
giving name 'a' is declaring
= is assignment operator
10 is the initialization

In python no need to mention data type.

Declaring multiple variables:
a, b, c = 5, 10, 15
name, price, weight = 'soap', 15, 10

If we want to declare multiple variables with same value:
x, y, z = 1, 1, 1
x = y = z = 1


# Python Dynamically Typed
What are the data types provided in python?
For eg in other languages: int, float, char

Python is dynamically typed.
x = 25
25 is integer type. x also becomes integer type then.
Remember x is just a reference to the data.
In python value has data type. But the variables don't have any data type. Variables will just hold reference to data.

In python, the data will have its data type.
The variable will have the same data type as the data it holds.

x = 13.75
x is now float.
x = 'A'
x is then string type.

x is changing its type as the program flows.
Therefore, variables are said to be dynamically typed.

To find out type of a variable:
type(x)
class 'int'
Note: Everything in python is an object and has a class.
int is a class. and x is an object of this class.

Variables don't have a type.
Type of variable depends on the value it references. If the value changes, then the type of a variable also changes, it is dynamic.


# Rules for Declaring Variable Names

1. Name can contain alpha-numeric characters and underscore.
2. Name should start with a letter or underscore character.
3. Keywords should not be used.
4. Variables are case-sensitive.

Program contains words. These can be classified into two:
1. Identifiers - defined by programmer
2. Keywords - predefined by the language

Keywords are reserved and cannot be used as identifiers.


# Python Data Types
Lot of data types in python:

1. Numeric - can support only a single value
    a. int
    b. float
    c. bool
    d. complex

2. Sequence - can hold collection of values. Values are ordered.
    a. list - ordered sequence of objects
    b. tuple
    c. string - ordered sequence of characters.
    d. bytes - immutable. Others can contain any type of data but these contain only 1 byte of data. So each value can be only between 0-255.
    e. bytearray - mutable

3. Set - collection of values. But the values aren't ordered.
    a. set - mutable
    b. frozenset - immutable

4. Dictionary - key value pairs
    a. dict


# Numeric Datatypes: int and float
Numeric datatypes:
1. int - integer values. No range limit for int values.
2. float - decimal values
3. bool
4. complex

## Ints
There is no fixed size memory taken by any datatype in python

a = 125
b = 2164
x = 12345678901234567890123456789

print(x.__sizeof__())
40

Python treats everything as an object, so it has its own way of consuming memory.

Suppose that we do
a = 125
Then data 125 is stored in memory. a is a reference to 125.
Now if we do
a = 200
Then 125 is not modified. 200 is a new value which is stored in a separate memory location and a will then point to the new memory location.
Note: Therefore, the value is immutable.

In python for most of the data types the values (data) are immutable.

What happens to the value 125?
It is collected by garbage collector.

## Floats
a = 12.59
in scientific notation as: 0.1259e2 or 1259e-2
Value before E is mantissa after E is exponent.

There is no limit on range of float type also. It can take any value.

Float values are also immutable.


# Numeric Datatype: bool and complex

## Bool
bool is logical data.
1. True - 1
2. False - 0
True means 1. But 1 cannot be used in place of True.
That is the vice versa is not correct.

This is because booleans are numeric datatypes in python.
False is an object of bool class which is a subclass of int.

Remember 1 will be int class object but True will be of class bool.

## Complex
a + bj
x = 3 + 5j
x = complex(3, 5)
x = complex(12)
x is then 12 + 0j
x.real = 3
x.imag = 5

j follows from the electrical engineering convention. Also, from the python forum discussions: Guido van rossum: i and I look too much like numbers...etc.
Not too clear. But j is what we get.


# Literals or Constants
Literals are the direct values or data written in the program.
We use variables for storing data.
x = 250
250 is a literal.

price = input("Extra price")
So this is another method of getting data into the program.

If we give
price = 250
whenever we run the program it will be the same.
It is therefore called a constant or literal.

Python allows literals for the following types.:
int
float
complex
string
bool

int literal.
    a = 125
    b = 12_5200
_ here works like , in usual mathematical notation.
But 125_ is not allowed as _ is used to separate digits.

float literal.
    a = 12.59
    b = 13.0 - if we write 13 it will be an int.
    c = 1.32E2
    d = 123_779.45
    e = 123.4_5
We can use _ in float integer and decimal part as well.
But 123_.45 or 123._45 are NOT allowed as _ is used to separate digits.

bool literal.
    a = True
    b = False

complex literal.
    a = 5 + 4j
    b = 5_1 + 4_3j

str literal
    a = 'john'
    b = "john"
    c = '''john'''
All of ', ", ''' can be used to define string literal.
We will see this in-depth later.

Note: There is no character datatype in python.

We will see more ways of defining literals later.


# Integer Literals

Integer (only integer) literals can be represented in different number systems.

a = 10. decimal
a = 0b1010. binary
a = 0o12. octal
a = 0xA. hexadecimal

a = 0b125. This will throw an error.

Can float value be given using other number system. Eg something like f = 0b111.0b11?
NO. This is not allowed.

Can complex value be given using other number system?
c = 5 + 6j
c = 0b101 + 6j?
Yes, this is allowed.
Note: Here only the real part can be given using any other number system. The imaginary part has to be given using the decimal system.

## For inputting values in other number system
price = int(input("Enter price"), 2)
Here 2 will be used as the base for type casting.


# Base Conversion

Base conversion functions:
- bin()
- oct()
- hex()

a = 10. We want to know the binary form of 10.
x = bin(a)
x will be a string that will contain the binary form of a.

Even the following works:
hex(True) -> '0x1'
bin(True) -> '0b1'
But the following will not work:
bin(12.5) -> Error

Only int and bool types are allowed as inputs to these functions.


# Type Conversion
Converting data from one datatype to another.
- int()
- float()
- complex()
- bool()
- str()

There are two types of type conversion:
1. Implicit - done automatically by python
2. Explicit - done by programmer

i = 15
f = 16.59
b = True
c = 10 + 6j
s1 = 'john'

# int
x = int(f) -> x = 16.
The decimal part is removed.
x = int(b) -> x = 1.
x = int(c) -> Not possible.
x = int(s1) -> Not possible.
But the following will work.
s2 = '125'.
x = int(s2) -> x = 125.
A string can be converted to integer if it only contains digits.

s3 = '0b1111'
x = int(s3, 2)

# float
x = float(i) -> x = 15.0
x = float(b) -> x = 1.0
x = float(c) -> Not possible.
x = float(s1) -> Not possible
x = float(s2) -> 125.0

# complex
x = complex(i) -> x = 15 + 0j
x = complex(f) -> x = 16.59 + 0j
x = complex(b) -> x = 1.0 + 0j
x = complex('10 + 6j') -> x = 10 + 6j
Therefore this is another way of creating a complex number.
x = complex(10) 
x = complex(5, 6). Real and imaginary parts. -> 5 + 6j

# bool
Works on all the datatypes. If value is 0 it will be false otherwise will be true.
x = bool(i) -> x = True
x = bool(f) -> x = True
x = bool(0+0j) -> x = False
x = bool('125') -> x = True

x = bool('True') -> x = True
bool works with any kind of string.
bool('') -> False.
Any other string gives a true value.
bool('haha') -> True.
Its like it returns false for empty string and true for non-empty string.

# str
works on any datatype.
