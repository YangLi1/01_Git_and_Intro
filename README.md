Author
==========
"Gardner, Daniel", gardnedn
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

Yes, it is okay to have the local copy of my repo on a USB drive and carry it around, but this is more risky. It's legal because you can sync with github from anywhere, but this method is less practical simply because we could lose the local repo. Keeping it on the M: drive is much safer and is still legal, and is therefore prefered.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Clone the repo from github that way I can work on it from the local machine. Of course I would have to have commited all my work from before so that way id be working on the current version.

#### 3. Morin, Exercise 1.1 (p. 23)
1. by pushing all the elements onto a stack and then popping them all off and putting those popped elements into an array list, they will be reversed 

	
2.  using a for loop of  for (int i=0,  i= size/50, i++) to make it run through however many sets of 50s there are and then nesting  {  
for (int j=(i+1)*50, j> ((i+1)*50)-50 , j--) to print out that  multiple of 50 from 50 to 49 ect.
}

3.  i would use a queue then pop off the first one after the size of the queue is 42 and add the current line at that time. then when the line is blank save the oldest item in the queue and report that.
 
4.  Using a list, run through the list, and if it's a duplicate, do not write it out.

5.  Using a list, run through the list, and if it has already been seen at least  once, then write it out.

6.  make a list, sort the list from shortest to longest, then print out the lines if the same line has not been printed already.

7.  make a list, sort the list from shortest to longest, then print out all lines in list.

8. make a list, read through the list twice, fist printing out the lines that are even, then run through a second time doing every odd line.

9.  read in all the lines into an array list, and then have it shuffle using random indexes. 



#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

CHOICE IS 1.4

by pushing all the elements onto a new stack and then popping them all, they will be reversed.


Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)


#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - binary data. "it references nothing and is referenced only by tree objects."
2. tree - Tree objects point to blobs and possibly to other trees as well. A tree is a new version of the same project after a commit or deviation from a branch
3. commit - an update or change a branch.
4. repo - the repository, where the code is located.
5. hash - the 40 digit assigned algorithem that references to a work.

