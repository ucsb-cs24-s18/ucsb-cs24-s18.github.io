---
layout: lab
num: lab06
ready: false
desc: "Evaluating expressions with stacks"
assigned: 2018-05-22 09:00:00.00-7
due: 2018-05-29 23:59:00.00-7
---

# Goals for this lab

By the time you have completed this lab, you should be able to

* Understand the purpose and behavior of a priority queue
* Understand how to implement an array-based heap

This lab may be done with a partner

## Step by Step Instructions

## Step 1: Create a lab06 git repo and get the starter code

First get together with your lab partner. If your regular partner is more than 5 minutes late, let your mentor know.

Select a pilot, log into the CSIL machines.

## Step 1a: Create a git repo, add your partner as collaborator

* Create a repo for this lab on the pilot's github account (just like you did in lab00): To do this, open a browser and navigate to [www.github.com](www.github.com). Log into the pilot's github account. From the drop down menu on the left, select our class organization: ucsb-cs24-s18 and proceed to create a new repo. You may refer to the instructions in lab00. Follow this naming convention: If your github username is jgaucho and your partner's is alily, your should name your repo lab06_agaucho_alily (usernames appear in alphabetical order). Also you must set the visibity of your repo to be 'PRIVATE' when creating it. We will not repeat these instructions in subsequent labs.

* The pilot should add the navigator as a collaborator on github, and the navigator should accept the request to join the repo. See instructions in previous labs

## Step 1b: Clone your git repo and get the starter code

* Clone your repo in your cs24 directory on CSIL. If your repo is called lab05_jgaucho_alily, type the following commands:

```
cd ~/cs24
git clone git@github.com:ucsb-cs24-s18/lab06_jgaucho_alily.git
```

Now navigate to your starter-code directory (cloned in a previous lab) and do a git pull to get the latest version of the code

```
cd ~/cs24/cs24-s18-lab-starter-code/
git pull
cd ~/cs24/lab06_jgauch_alily/
```

Now copy all of the files for this lab from the starter-code directory to your git repo directory:

```
cp ~/cs24/cs24-s18-starter-code/lab06/* ./

-bash-4.3$ ls
examheap.cpp heap.cpp heap.h
```

First look at heap.h to see the basic operations for a heap. You will implement all of these operations for these lab. Also notice the storage mechanism we will be using for the heap: a [http://www.cplusplus.com/reference/vector/vector/](vector). It will probably be a good idea to read through the documentation for this standard library class (linked above) if you are not familiar with it.

Now look at examheap.cpp. This file will test your heap's behavior. The first test is quite simple and just adds a couple elements to your heap. For larger numbers of inputs, it uses the `std::priority_queue` class from the standard library as ground truth to test your code against. The first thing you need to do is compose your Makefile to compile `examheap.cpp` with `heap.cpp` to executable `examheap`. Then, feel free to compile and run `examheap` before starting on your code. However, note that all the tests will fail and say "Aborted (core dumped)".

## Step 2: Implement the functions of heap.cpp

There are four functions you need to implement in heap.cpp: `push`, `pop`, `top`, and `empty`. Note that only `push` and `pop` modify the heap, while `empty` and `top` only return values. When testing your code, be sure to run the large tests (4 and 5) to find any minor bugs in your code that may not show up on the smaller tests.

You are allowed to add helper functions in heap.h and heap.cpp if you need them. However, you should use the vector in heap.h as the underlying storage for your heap.

## Step 3: Submit heap.cpp and heap.h

Submit the files heap.cpp, heap.h, and Makefile to the lab06 assignment on Gradescope.

## Evaluation and Grading

Each student must accomplish the following to earn full credit for this lab:
[70 points] heap.cpp and heap.h are saved, with your name(s) in a comment at the top and other evidence of your work. Both of these files should compile and execute properly too.

To be eligible for late turn-in with credit, you MUST have attended your entire lab period.
[-0 to -55 points, at the mentor's discretion] The student arrived on time to their lab session, and worked diligently on CS24-related material until dismissed.
