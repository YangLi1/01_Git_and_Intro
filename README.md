Author
==========
"Kojs, Michelle", kojsmn
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

It is okay to keep the local copy of your repo on a USB drive and M: drive. A local copy of your repo needs to be made so that you can make changes to it and then push these changes to GitHub.
Whether you decide to keep it on your USB drive or M: drive is up to you. As long as you can access it to make changes.


#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Since you forgot your USB drive with your repo on it, you can make a local copy of the most recent repo by cloning the repo from GitHub and store it on your M: drive. Hopefully you pushed your
most recent changes that you did on your USB drive to GitHub.

#### 3. Morin, Exercise 1.1 (p. 23)

1. Stack: Stack allows for a last-in-first-out method so use this to print the lines in reverse.
2. List & Stack: in List multiple lines of input can be added at one time, then use Stack to remove the lines in reverse order
3. List: read the first 42 lines and then get(i) each next line and see if blank. If blank then get(i) the blank line minus 42 and output.
4. USet: USet does not allow duplicates. Read each line and before adding it use find(x) to see if the line has already been read. If it has do not add but if it has not then add.
5. USet & List: USet does not allow duplicates. add(x) each line one at a time and if the line already exists in the USet (find out through find(x)), add the line to a List
6. SSet: Use the compare(x,y) to sort the lines and remove duplicate lines through find(x).
7. SSet: Use the compare(x,y) to sort the lines
8. List: Add all the input and then output the even through get(i) and a for loop, then output the odd
9. USet: USet is an unordered set of unique elements. Use random number to randomly pick i and get(i)

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.2: A relationship between Dyck words and Stack push(x) and pop() operations is the addition and removal of +/- 1's to get a Dyck word. Stack push(x) and pop() operations can be used to ensure that the prefix of a Dyck word is positive. An if statement can be run where if the prefix is negative, a +1 must be added through Stack push(x) in order to make a Dyck word. If the prefix is not negative then it is a Dyck word.

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - represented by each version of a file; holds only the file's data; does not contain any metadata about the file or its name.
2. tree - represents one level of directory information; can reference other tree objects
3. commit - holds metadata for each change in a repo; points to a tree object; have parents except the inital commit has no parent
4. repo - database that contains all the information needed to retain and manage the revisions and history of a project
5. hash - 40 bytes of hexadecimal that represents a file; once a file is changed a hash is changed
