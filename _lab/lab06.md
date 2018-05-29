---
layout: lab
num: lab06
ready: true
desc: "Implementing a heap"
assigned: 2018-05-30 09:00:00.00-7
due: 2018-06-05 23:59:00.00-7
---

# Goals for this lab

By the time you have completed this lab, you should be able to

* Understand the purpose and behavior of a priority queue
* Understand how to implement an array-based heap

This lab may be done with a partner

## Step by Step Instructions

# Step 0: Complete the TA/Mentor evaluations
As you may know, we ran a pilot mentor program this quarter.
We would like to get your feedback about the program to help us keep the aspects that worked well and identify areas for improvement.

Completing the survey carries course credit (1% of your overall grade), so please be sure to complete it. This is an anonymous survey. To get credit please show the final screen  to the instructor TA/tutor

Here is the link to the survey:
[Please click on this link to complete](http://bit.ly/2018-Anonymous-Mentor-Evals)

You may use the following webpage to identify the mentors should you need it to answer the final question on the survey:
[https://ucsb-cs24-s18.github.io/info/staff/](https://ucsb-cs24-s18.github.io/info/staff/)

To get credit show the final screen of the completed survey to your mentor and ask them to update your grade on gradescope.

**The remainder of the lab is on the heap data structure. We will talk about this data structure on Wednesday's lecture, so while you are welcome to read the writeup and go over the starter code, please don't attempt this lab unless you are already familiar with using the heap data structure. Instead, wait until we have covered the material on Wed. You may use the lab time to work on pa02**

## Step 1: Create a lab06 git repo and get the starter code

First get together with your lab partner. If your regular partner is more than 5 minutes late, let your mentor know.

Select a pilot, log into the CSIL machines.

## Step 1a: Create a git repo, add your partner as collaborator

* Create a repo for this lab on the pilot's github account (just like you did in lab00): To do this, open a browser and navigate to [www.github.com](www.github.com). Log into the pilot's github account. From the drop down menu on the left, select our class organization: ucsb-cs24-s18 and proceed to create a new repo. You may refer to the instructions in lab00. Follow this naming convention: If your github username is jgaucho and your partner's is alily, your should name your repo lab06_agaucho_alily (usernames appear in alphabetical order). Also you must set the visibity of your repo to be 'PRIVATE' when creating it. We will not repeat these instructions in subsequent labs.

* The pilot should add the navigator as a collaborator on github, and the navigator should accept the request to join the repo. See instructions in previous labs

## Step 1b: Clone your git repo and get the starter code

* Clone your repo in your cs24 directory on CSIL. If your repo is called lab06_jgaucho_alily, type the following commands:

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

First look at heap.h to see the basic operations for a heap. You will implement all of these operations for these lab. Also notice the storage mechanism we will be using for the heap: a [http://www.cplusplus.com/reference/vector/](vector). It will probably be a good idea to read through the documentation for this standard library class (linked above) if you are not familiar with it.

Now look at examheap.cpp. This file will test your heap's behavior. The first test is quite simple and just adds a couple elements to your heap. For larger numbers of inputs, it uses the `std::priority_queue` class from the standard library as ground truth to test your code against. The first thing you need to do is compose your Makefile to compile `examheap.cpp` with `heap.cpp` to executable `examheap`. Then, feel free to compile and run `examheap` before starting on your code. However, note that all the tests will fail and say "Aborted (core dumped)".

## Step 2: Implement the functions of heap.cpp

There are four functions you need to implement in heap.cpp: `push`, `pop`, `top`, and `empty`. Note that only `push` and `pop` modify the heap, while `empty` and `top` only return values. When testing your code, be sure to run the large tests (4 and 5) to find any minor bugs in your code that may not show up on the smaller tests.

You are allowed to add helper functions in heap.h and heap.cpp if you need them. However, you should use the vector in heap.h as the underlying storage for your heap.

## Step 3: Submit heap.cpp and heap.h

Submit the files heap.cpp, heap.h, and Makefile to the lab06 assignment on Gradescope.

## Evaluation and Grading

Each student must accomplish the following to earn full credit for this lab:
[70 points] heap.cpp and heap.h are saved, with your name(s) in a comment at the top and other evidence of your work. Both of these files should compile and execute properly too.


