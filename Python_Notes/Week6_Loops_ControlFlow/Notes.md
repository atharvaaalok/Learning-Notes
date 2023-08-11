# Section Introduction
We will learn about:
- while loop
- for loop
- continue, break, pass
- infinite loop
- match case

# Introduction to loops
These are of two types:
- while loop
- for loop - also called foreach loop

```python
while condition:
    execute statement 1
```

The loop will execute until the condition remains True. The condition can also be a number not equal to 0 as discussed before.

# Infinite loop - break - continue - pass
pass can be used with `if` statements also but, break and continue cannot be.

`pass` is usually a "to do" placeholder. In Python you cannot declare functions without implementation or any code block without a body, for example if condition: (do nothing), so you just put pass there to make it valid. `pass` does nothing.  

Other uses of pass:


# else suite
else can be written with:
- if
- while
- for
- try

```python
while condition:
    statement 1
    statement 2
else:
    # If the condition was/becomes false then this else block is executed.
    # If the condition never becomes false, eg: using break, then else will not be executed.
    # This can be used to check if while was executed completely.
```

# for loop
iterates over a sequence object.

```python
msg = "Hello"
for x in msg:
    print(x)
```

This loop repeats for each value in a sequence. Hence it is similar to a foreach loop.  

# range
range is a function  
range(n) returns the numbers: 0, 1, 2, ..., n-1.  
range(n1, n2) returns: n1, n1+1, ..., n2-1.  
range(n1, n2, s) returns: n1, n1+s, ..., the last number smaller than n2.  
range(n1, n2, -1) returns: n1, n1-1, n1-2, ..., n2

# Membership operators - in, not in
`in` and `not in` are membership operators.  
They allow us to quickly determine if a given value is or isn't part of a collection of values.  

**Note:** Don’t confuse the in keyword when it works as the membership operator with the in keyword in the for loop syntax. They have entirely different meanings. The in operator checks if a value is in a collection of values, while the in keyword in a for loop indicates the iterable that you want to draw from.

# for else
works similar to while-else.  
else runs if the for loops ends properly and not with break command.

# Match case
similar to switch case as in other languages.  

example:
```python
day = int(input('Enter Day number'))

if day == 1:
    print('Sunday')
elif day == 2:
    print('Monday')
elif day == 3
    print('Tuesday')
else:
    print('Holiday')
```

Same thing using match case:
```python
day = int(input('Enter Day number'))
match day:
    case 1:
        print('Sunday')
    case 2:
        print('Monday')
    case 3:
        print('Tuesday')
    case _:
        print('Holiday')
```

It doesn't work like switch case as in other languages.  
In switch case the program directly jumps to the particular case number, here it goes through each case and checks if that case matches.  

the match datatype can be anything.