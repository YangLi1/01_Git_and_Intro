Author
==========
"Decker, Benjamin", deckerbd
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

It's okay to make copies of your work and back it up also using your USB drive or M drive, but it's not okay to use them as your master for your work. It's important to use redundancy when backing up your master, and using GitHub to keep copies of all your repos online where you can access them anywhere.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Clone your up-to-date repo from GitHub using git, check it out, work on it, then push your updates while you work to GitHub.

#### 3. Morin, Exercise 1.1 (p. 23)

1.1.1. Stack: using a loop, read in each line as a string, and push it onto a stack. Once all the lines are read, use a loop which pops a string off the stack and prints it.

1.1.2. Stack: using a loop which reads in 50 lines as a string, push each line onto a stack. Once 50 lines are read, use a loop which pops a string off the stack and prints it.

1.1.3. Queue: first read in at least 42 lines, placing them into a queue capable of storing 43 lines, while discarding any blank lines and popping without printing if the array reaches 43 lines long. After having stored 42 lines, instead of discarding blank lines, if a blank line is detected, pop and print the line.

1.1.4. USet: add each string into a USet since the USet will only add unique elements. If the add(String s) returns true, print the string.

1.1.5. USet: attempt to add each string into a USet. If the add(String s) returns false, print the string.

1.1.6. SSet: add all the lines into the SSet, which will automatically sort them, while also refusing to accept duplicates, then print the output.

1.1.7. USet: add all the strings into a USet, then print them all out.

1.1.8. 2 Queues: alternate adding each line to the queues, so that one queue has all the even numbered lines, while the other has all the odd numbered lines. Print the contents of the even one first by popping and printing, then do the same with the odd numbered queue.

1.1.9. Array of Strings: load each string into the array, then use Math.Random() to generate a random number in the array to print, while keeping track of which integers were already picked.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

Exercise 1.4:

 while(!stack.isEmpty())
  queue.add(stack.pop())
 while(!queue.isEmpty())
  stack.push(queue.next())


#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - An allocated space of files
2. tree - a directory consisting of pointers to blobs and other subdirectories/trees
3. commit - a version of your project which contains a pointer to its parent and a pointer to the directories/blobs being used by this version.
4. repo - the database filled with your objects which contains configurations and histories of your project
5. hash - the identifier for an object; the name is calculated using SHA1 and is represented with 40 character hexadecimal encoding

* Some of the definitions above were found in the gitglossary, which can be found here: https://www.kernel.org/pub/software/scm/git/docs/gitglossary.html
