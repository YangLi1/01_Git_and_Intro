Author
==========
"Griffith, David", griffid5
01_Git_and_Intro
================

Practice with basic git functions, and intro to study of Data Structures

Reading
=======

**Version Control with Git, 2nd Ed**. Loeliger and McCullough. 

http://proquest.safaribooksonline.com/book/databases/content-management-systems/9781449345037/version-control-with-git/id302681?uicode=ohlink (Free access through www.lib.miamioh.edu, but limited to 100 simultaneous users across all OhioLink. I recommend downloading/printing the required readings ahead of time, just in case.)

Read only the following:

1. Chapter 1
  * Background
  * The Birth of Git
2. Chapter 3: Getting Started
  * Intro
  * The Git Command Line
  * Quick Introduction to Using Git (read all sections)
  * Configuration files (Intro only, may skip part on aliases)
3. Chapter 4: Basic Git Concepts
  * Basic concepts (read all)
  * Object store pictures
  * Git concepts at work (read all)
4. Chapter 21: Git and Github

**Open Data Structures in C++**. Morin. 

http://opendatastructures.org/ (Free access. I recommend downloading the PDF version.)

Read the following:

1. Chapter 1 (pp. 1-20)

Homework
========

1. Create an account with github.com. You may select the free account. If you want to get some free private repos, you may apply at https://github.com/edu
2. Go to https://github.com/MiamiOH-CSE274/01_Git_and_Intro and fork the repo, which will create a copy of it in your github account.
3. Install git on your computer, if you do not already have it. I recommend installing http://windows.github.com/ if you use windows, or http://mac.github.com/ if you use Mac. HOWEVER, I highly recommend using the command-line tools for everything, and ignoring the GUI. I will not be providing help with configuring/using the GUI.
4. Clone your repo from github to your computer. When you are at the web page for your repo, `https://github.com/[your github id]/01_Git_and_Intro`, you will see info about how to clone it. The easiest way is to go to the command line terminal, and type `git clone git@github.com:[your github id]/01_Git_and_Intro.git`
5. Checkout your personal branch from the repo. Each student has a branch labeled by their Miami uniqueid. `git checkout uniqueid` ... for example, I would do `git checkout brinkmwj`
6. Complete the exercises below by modifying this file.
7. After you complete each answer, be sure to create a new commit with the changes (using `git add README.md` and `git commit -m` as appropriate). Also, be sure to upload to github frequently by using `git push`
8. If I don't see at least 4-5 commits on this homework, I'm going to be unhappy.
9. Once complete, send me a pull request. You should send from your branch in your github repo, to your branch in the MiamiOH-CSE274 repo. This is your official "turn in" of the homework, which I will grade.
10. Double check that you did the right thing by going to https://github.com/MiamiOH-CSE274/01_Git_and_Intro/pulls and making sure that your pull request is there, and looks like you expect. Optimism is the root of all evil.

Exercises
=========

#### 1. Based on the reading in the Git book, is it okay to keep your local copy of your repo on a USB drive and just carry it around? Explain why or why not. What about keeping it on the M: drive?

After reading the Git book I believe it is a good idea to keep your local repo on a USB drive or the M drive because you can still work on your project even if you can't get access to the Github website. With that said you still need to make sure your latest copy of your repo is also uploaded to the Github website before closing out your work on your local drive if possible. This will ensure that you have the latest copy both locally and on the web.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Since you should have uploaded your latest version to the github website, you should go the the github website and clone your latest version to your local machine. 

#### 3. Morin, Exercise 1.1 (p. 23)

1. The data structure that I would use is LIFO (last-in-first-out). I would use this data structure because you are reading an input one line at a time and then you want to print the lines in reverse order which means that the last line read-in should be the first one out which is the functionality of LIFO. 

2. For this problem I would use both FIFO and LIFO (DEQUE). If we group the 50 lines of code into batches we can see how this will work effectively. Each batch of 50 lines are going to use the LIFO method within themselves, however, once the second 50 lines of code (2nd batch) is introduced you will place them beyond the first batch which utilizes FIFO method. Basically the second batch would be queued beyond the first batch which means that the first batch would read line 50, 49 etc then after it completes the 2nd batch would start at 99, 98 etc because we used LIFO in the individual batches and FIFO over all batches (whole system).  

3. Since order matters in this question I would use SSet. I would have it read in 43 lines then search for a blank line and if found go back 42 lines and print. Otherwise read another 43 lines and do the same thing until all lines have been read. 

4. I would use a USet structure for this problem because in a USet no element can appear more than once. Also order doesn't matter and the USet will contain n distinct elements which will help with memory since you are not able to take in duplicate items. 

5. I would use a USet structure for this one as well for the same reasons as question 4.

6. A SSet structure would work well for this problem because we want the lines sorted by length in which a SSet allows us to comepare two elements. Much like the USet there cannot be duplicate lines so we don't have to worry about the same line being printed twice. 

7. A priority queue would be good in this situation since you can have duplicates and it will print the smallest (shortest in this case) element from the list. 

8. By using a Deque we can print line 0 by removeFirst(). After that we can removeFirst() + (an incrementaion variable) that jumps us to all the even locations. Once we run out of even locations we can removeFirst() + (odd incrementation variable) and print out all the odd lines. 

9. I would use a Deque because you can add to the front (addFirst(x)) and the back (addLast(x)) of the queue which if you call each operation randomly, you will randomize the order before they are printed. 

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)
 
Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

Exercise (1.4) To reverse the order of the elements in Stack (s) you are going to do the following:
1. pop() the first element off s. 
2. add(x) the first element that was poped from s to q.
3. repeat (loop) steps 1 and 2 until all elements have been removed from s.
4. remove() the first element in q (which should be the first element that was poped from s) 
5. push (x) the element that was removed from q to s. 
6. repeat(loop) steps 4 and 5 until all elements are in reverse order in s.  


#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A blob is the contents of a file. Blob names are unique, meaning that there is only one name for each blob. 
2. tree - A tree in git helps to keep track of what files we have. It points to blobs and other trees. 
3. commit - A commit does 3 primary things in git. First it makes a new commit object that holds metadata (author, committer, commit date and log message). Secondly, it makes a new blob if things have changed in a file. Latestly, it makes a duplicate tree and points to the same blobs in the previous tree if the contents didn't change in the blob, if contents did change it points to the new blob that contains the new changes. 
4. repo - In git the repo keeps track of the entire project from start to finish. It contains all information so that a complete working copy of all the files can be used. 
5. hash - A hash in git is a long string that takes 40 bytes of hexadecimal to produce in which each hash is unique. Each hash is assigned to a blob in which no two blobs will theoretically (at least in github) have the same hash value. An example of a hash in git is 3b18e512dba79e4c8300dd08aeb37f8e728b8dad.  