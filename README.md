Author
==========
"Zirkle, Andrew", zirkleac
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
  * Repo for Public Code
  * Creating a GitHub Repository
  * Forks
  * Creating Pull Requests
  * Managing Pull Requests
  * Coding Models

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

No, it is really easy to lose a USB drive, the M Drive is safer because it is backed up repeatedly, but having it backed up online is the safest.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

git pull latest version

#### 3. Morin, Exercise 1.1 (p. 26)

1.read the file backward, printing each line
2.if new lines exist(read lines into array, print them out backward from the last of the array if greater than 50, clear array )
3. read new lines if line == "" move pointer+100lines print line, move pointer back 100 lines
4.read line, if line != arrayOfUniqueLines(all) add to array OfUniqueLines, print unique liens
5.readline, if line != arrayOfUniqueLines(all) add to array OfUniqueLines, print all other lines
6.copy 4 shell sort by size
7.read line shell sort by size
8.read all lines, get count/2 if if count ==0 end, else{ if( line.getCharcterCount/2==0) output line;) else(move line to back)} print remaining lines// the odd numbered ones  
9.read all lines, get random number; get random line; print random line; remove random number in array;

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

you would from the bottom of the stack add to the top of the queue, and then remove the bottom of the stack, doing this in a loop until the stack was empty
then you would remove all the items in the queue back into the stack

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - a binary large object, it contains a  version of the file
2. tree - a level of directory information with blob identifiers and path names
3. commit - hold meta data about the changes sumbitted to the repository
4. repo - short name for a repository, holds the main version of the files which people work off of and submit changes to
5. hash - a unique identifier for a commit and the files inside
