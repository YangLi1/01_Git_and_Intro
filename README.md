Author
==========
"Monnin, Sebastian", monninse
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

No that is not ok. It is not ok because it deprives other people of getting to see and use your work. It also put your work at risk of being lost if there is a failure with your USB or M: drive.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

You clone the homework offline and start working on it again from scratch. But from then on you don't save things on a USB drive you use git and github to help keep track of all your work over the time you work on it.

#### 3. Morin, Exercise 1.1 (p. 23)

1.I would use a LIFO Queue. I feel that this would be the best data structure because it is for last in first out. Which is exactly what the problem is asking for.
2.I would again use a LIFO Queue. I would use two for loops. the top loop would iterate 50 times and within each iteration it would read one line of text and check to make sure there was a next line of text. once the first loop had gotten to 50 the second loop would print everything back out and then the loops would start back over from a while loop inclosing the two for loops
3.I would use a LIFO queue. I would use a while loop to read and store lines of code. If there is ever a blank line then it prints all 42 lines of code that are stored. It can never store more than 43 lines so it always throws away the oldest line to store the newest line of code
4.I would use a while loop to keep reading a storing all of the inputs, during each iteration before I outputted the input I would use find(x) to check and see there were any identical lines of code that had already been input
5.I would use a while loop to read and store each input. I would use find(x) to search through the inputs and if there was already one of something stored than I could output the line that was just input
6. Deque. I would use a while statement to read in every line. I would then store each line in an array list. I would then go through the array and bubble sort the array list by length. I would then go through the array list using while loop and an if statement to check and see if there are any lines of the same length, I would have it delete duplicates. then use a while loop to go back through and read the lines in length order
7. Deque. I would use a while statement to read in every line. I would then store each line in an array list. I would then go through the array and bubble sort the array list by length. I would then go through the array list using while loop and an if statement to check and see if there are any lines of the same length,. If there are lines of the same length I would use a for loop and an off statement to print the lines ,how ever many times they showed up in the input process, during the output process
8.I would use the last in first out approach. I would use 2 for loops. The first for loop would input each even numbered line and inside that for loop there would be a while loop so that after the for loop had gone to the end of the input it would print them all back out in normal order. After that the second for loop would do the same thing only with odd numbered lines.
9.I would use a while loop. During each iteration of the loop a line would be input and add(x) would be used to store the line, also during each iteration a counter would increase by 1. I would make the storing of the lines random by using a random number generator to in place of x in the add(x). The random number would be in-between 0 and the number of lines stored. Then at the end I would use a while loop to print all of the lines out.

### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

1.3

A stack is last in first off approach. So I would use a while loop to cycle through the characters of the string and during each iteration it would check to see if the character being looked at is the same as the one after it. I would do this by using .equals to compare the current and next character in the string.The program would compare the character being added to the stack to the one getting popped off.



#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - In Git each version of a file is represented as a blob. A blob holds a file’s data but does not contain any metadata about the file or even its name.
2. tree - A tree object represents one level of directory information. Inside a tree are blobs
3. commit - A commit object holds data about changes into a repository. A commit points to a tree that captues the state of the repository at the time the commit was performed.
4. repo - A repository is a database containing all the information needed to retain and manage the revisions and history of a project. In git a repository holds a complete copy of a project through its entire lifetime
5. hash - Hash in git is like the address or the name git gives to a file to help keep track of it