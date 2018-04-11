---
num: "lect04"
desc: " Operator overloading, Makefiles, gdb, pa01"
ready: true
pdfurl: /lectures/CS24_Lecture4.pdf
annotatedpdfurl: /lectures/CS24_Lecture4_ann.pdf
annotatedready: false
lecture_date: 2018-04-11
---

# Code from lecture

[https://github.com/ucsb-cs24-s18/cs24-s18-lectures/tree/master/lec-04](https://github.com/ucsb-cs24-s18/cs24-s18-lectures/tree/master/lec-04)

# Topics

## gdb

* Demo of gdb commands using example from lab02
 - To use gdb, compile with the -g flag
 - Setting breakpoints (b)
 - Running programs that take arguments within gdb (r arguments)
 - Continue excution until breakpoint is reached (c)
 - Stepping into functions with step (s)
 - Stepping over functions with next (n)
 - Re-running a program (r)
 - Examining local variables  (info locals)
 - Printing the value of variables with print (p)
 - Quitting gdb (q)
 - Debugging segfaults with backtrace (bt)
* Refer to the [gdb cheat sheet](http://darkdust.net/files/GDB%20Cheat%20Sheet.pdf) (handout given in class). More practice in lab 02.

## Makefiles
* We will split our implementation of the die Game from the previous class into three files  - header file (contains only the class definition), source file (contains the implementation of the class methods - no main), test file - uses the ADT. (More practice on this in lab02)

## The big four
* Constructor
* De-constructor
* Copy-constructor
* Copy-assignment

## Operator overloading - Pages 63 - 80 in the book

We will start with a basic implementation of the point class from Chapter 2. We will then augment the class with binary operator functions. By **overloading** certain operators like ==, we can now write code as shown below:

```
point p1, p2;
if (p1 == p2){
  cout<<"Points are equal\n";
}
```
We will specifically discuss:

1. Overloading binary comparison operators e.g. ==
2. Overloading binary arithmetic operators e.g. +
3. Overloading output and input operators e.g. >> and <<

If time permits...

## Review of pointers and dynamic memory allocation
* Review of pointers, arrays
* Passing parameters by value and address
* Passing arrays to functions
* Dynamic memory allocation and dynamic arrays




