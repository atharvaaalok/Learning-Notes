# Course Contents:

Introduction to Python
Python Installation and Setup

Python Datatypes
Operators and Expressions
Conditional Statements
Loops-Control Flow

Strings and its Methods
Formatted Printing

Regular Expression

List
Tuple
Sets
Dictionary

Functions
More about Functions

Exception Handling
File Handling

OOP

MultiThreading
Date and Time
DataBase Connectivity
Data Structure Modules
Math Modules
OS ModuleFunctions
Tkinter Module
NumPy Module


# Types of Programming Languages

What do we mean by "Programming Languages"?

## Low-Level Language
Machine Language - What the machine understands
Assembly Language - ??

## High-Level Languages
General Purpose - C, C++, Java, Python
Special Purpose - HTML, CSS
Scripting - ??

Eg: C
C - what we understand, ML - What the machine understands.
Compiler - compiles the C program into ML. That can then be understood by the machine.


# Compiler vs Interpreter
High-Level Languages:
Compiler Based - C, C++
Interpreter Based - php, JS
Hybrid - Python, Java, C#

High language has to be translated to machine language.
Translation done by compiler or interpreter.

Compiler:
Program.c(source code) -> Program.exe(machine code)
1. Takes complete source code and converts to complete machine code.
2. If there are no errors in your program only then this translation is done.
3. Translation is done only once.
4. Show all errors and warnings at same time.
5. Debugging is slow.
6. Execution time is faster as no error checking which has been removed once.
7. Source code is private.
8. Source code is for particular machine (windows, mac etc.). Not cross-platform.
9. Compilation is an extra step we need to take to check our program.

Interpreter:
Program.js(source code) -> Runtime Environment -> No separate machine code file.
1. Takes lines of source code one by one and then translate to machine code.
2. No new file is generated.
3. Everytime we run the program the translation is done.
4. Error occurs after scanning each line.
5. Debugging is faster.
6. Execution time is slower as error checking takes time.
7. Source code is not private.
8. Source code is given and conversion done on a different machine.
9. Easier to test. Change a particular line and go.

Compiler was completing translation but not running. Interpreter runs the file also.

Therefore, mostly compiler based languages are faster than interpreter. But these days it doesn't make much difference.

Nowadays, interpreter based languages are preferred as they are more flexible.
It provides a runtime environment.

Hybrid Compilers:
Compiler as well as interpreter.
Program.py(source code) -> compiler -> Program.pyc(byte code) -> Interpreter (Runtime Environment) -> On machine

Command: python Program.py
python calls compiler.

Byte code file is only in memory not on hard disk.

Byte code is error free.
Byte code then goes to Interpreter which no longer has to check for errors.
May be line by line or directly to ML then execute. If all at once then its called Just In Time (JIT) compilers.

Runtime environment -> Python Virtual Machine

# Python: Platform Independent
byte code file is not executable.
It is translated by interpreter.
That can be done on the machine on which to run. Can be run only if PVM is available on the machine.
PVM itself is platform dependent.


# Programming Methodologies
Functional/Procedural Programming
Object-Oriented Programming
Modular Programming

Very difficult to manage large code so organize using one of these methods.

A program consists of: Data and Instructions for the data.

Functional - Breaks the large program into functions. Functions are independent of data and each function can take any data.
Function centric.

Object-Oriented - Breaks down large program into classes. Class consists data and functions that work on that data. Objects of those classes is used to make the bigger program.
Data centric.

Modular - Breaks down large program into Modules. Module consists of details of major task. Function is for specific task. Modules consist of classes and functions.

Smallest piece is function.
Class is slightly bigger.
Module is even bigger.


# Features of Python
Simple/Expressive
Easy to Learn
Scripting Language
Open Source - No license needed for commercial use. Also change python.
General Purpose - Libraries for lot of things.
Interpreted (Hybrid)
Platform Independent - CORA
https://youtu.be/RZ3vXsI1vDU
Portable - WORA
Procedural and Object Oriented
Dynamically Typed
Extensible - Inside python we can use code from other languages.
Embeddable - Inside other languages we can use python code.
Huge Library
Scalable


# Areas of Programming

GUI Programming
Web
Database
Enterprise
Network
Game
Multithreaded
Mobile
Machine Learning
AI
Data Science

Python provides libraries for each of these areas of programming.
Therefore, it is a general purpose language.

First learn about the area. Then the library for that.