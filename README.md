Author
==========
"Harvey, Steven", harveysd
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

No, it doesn't defeat the entire purpose of git, but it is a bad idea. You need to constantly be pulling, committing, and pushing your work to git's servers. This allows you to have an accurate representation of your changes. This also saves against loss of data, this goes for the M: drive as well. Data loss is a fact of life. If you just have your local repo on your flash drive or the M: drive and something happens to it, you are not going to have any recourse to get it back.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

You should just clone your repo from git's servers. You can then make whatever changes you need to make, and push your change. When you get back to your USB drive, you then can merge the two and fix whatever errors, if any, occur.

#### 3. Morin, Exercise 1.1 (p. 23)

1.1.1 
	
	create a stack
	
	open a file
	
	while the next input is a new line
		read in the line and put it on the stack
		check the next input
	
	while the stack isn't empty
		pop from the stack and write to the file
		check if the stack is empty
	
	close the file
	
1.1.2
	
	create a deque
	
	open a file
	
	create counter variable
	
	create boolean variable
	
	read in the first fifty lines
	
	while the next input is a new line
		if counter is factor of 50(50, 100, 150 etc)
			boolean = !boolean
		switch(boolean)
		if true (output the line from the front of the deque
				input the next line to the back of the deque)
		if false (output the line from the back of the deque
				input the next line to the front of the deque)
				
		counter +1	

	close file
	
1.1.3


#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

1.4

	for the stack size
		pop() each element out and put it in a queue
	for the queue size, push each element back onto the stack

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - the contents of a file in git
2. tree - the file directories of git
3. commit - points to the new tree
4. repo - repository, this is the overarching group of project files for any given project
5. hash - function that takes long strings and makes them short ones(this is an oversimplified answer)