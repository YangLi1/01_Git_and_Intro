Author
==========
"Contini, Nick", continnd
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

Most of the time a USB would be redundant to carry around unless you plan on working offline. It does not hurt, yet most of the time you should be able to have access to the Git server and whatever code you need.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Assuming you pushed your repository to github before leaving, you can pull your version of the repository to another computer.

#### 3. Morin, Exercise 1.1 (p. 23)

1. Using the LIFO interface, read the lines in order and then remove in reverse order
2. Using the List interface, I would read in lines until size() returns 50 or there are no lines. Then I would use get(size()-1) and remove(size()-1) to output and clear the array in reverse order. Once the array is clear again, repeat the process, unless the array never got to size 50.
3. Using the List interface, I would read lines one by one, and once the size() returns 43 or more, get(size()-1), and if it is blank, get(size()-42) and output it. Either way remove(size(-42) must be called at the end of the loop to make room for the next line.
4. Using the USet interface, read in every line, duplicates returning false during the add(x) function and not being added to the set. Then print the entire array.
5. Using the USet interface, read in every line, checking to see if the element is there using find(x). If it exists already, print the line. If not, it is added to the array.
6. Using SSet, read in every line. Duplicates will be found using find(x) and will be stored in a seperate list so that they get printed only once. The size of each string will also be checked as you add each string to the duplicate list in order to sort it as they are added.
7. Using SSet, do the same as #6 but now the duplicates list will also use find(x) so that if it is a duplicate of a duplicate, another list will be created and will then have to be checked.
8. Using the List interface, read in even numbers and remove and print them immediately, while odd numbered lines get stored until there are no more lines left and then are removed and printed.
9. Using the List interface, read in each line. When removing and printing, use remove(size()*random()) to remove a "random" line from the listing until size() outputs 0.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

1.3: If you store each character in the string in a list and get(n)==get(size()-n) ever outputs false, the possible values for n being from 0 to size()/2, then the string is an unmatched string. Otherwise it is a matched string.

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - binary data stored in a repository
2. tree - objects that point from blob to blob, or even other trees, connecting different versions. Represents a level of a directory
3. commit - an edit to a blob, that is followed by commentary of the changes between the previous and current version
4. repo - a place to store various parts of a project
5. hash - An identifier calculated by shrinking a long string from the blob to a small string