Author
==========
"Luo, Yu", luoy6
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

[Yes, it is okay to keep my local copy of my repo on a USB drive and just carry it around.]

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

[I will try to clone a repo from github.com]

#### 3. Morin, Exercise 1.1 (p. 23)

[1. Read the input one line at a time and then write the lines out in reverse order, so that the last input line is printed first, then the second last input line, and so on]
This can be accomplished by implementing Stack. Doing a pop() operation to remove the last line, and then print the last line on the screen. Doing a pop() operation to remove the second last input line, and then print the second last input line, and so on

	
	void function readAndReverse
		while the file is not empty
			do a pop() operation
			print the line that is removed by the pop() operation

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

[Exercise 1.4. Suppose you have a Stack, s, that supports only the push(x) and pop() operations. Show how, using only a FIFO Queue, q, you can reverse the order of all elements in s.]

The Stack, s, is a LIFO Queuing discipline. This means that if I do a pop() operation on s, I will get the last element on the Stack. 
On the contrary, q is a FIFO Queuing discipline. This means that if I do a add(x), where x = the element that is removed by s.  
	
	void function reverse
	while s is not empty
		do pop() operation on s
		do add(x) operation on q, where x = s.pop()


#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - Blob contains the contents of a file. A blob holds a file's data but does not contain any meta-data about the file 
2. tree - TODO
3. commit - TODO
4. repo - TODO
5. hash - TODO