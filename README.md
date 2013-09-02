Author
==========
"Vutisalchavakul, Pob", vutisat
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

Accidents may happen when you rely upon a USB drive, you may lose it, it make be physically broken, etc. Also git is better than using a an M: drive because it can update real-time to the server and can be access from anywhere.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

The only thing you may have to do is go back and get the USB if you did not use git, nor any type of storage over a server. However using github will solve this problem as you will be able to access it anywhere only with the requirement of internet connection.

#### 3. Morin, Exercise 1.1 (p. 23)

1) I think the stack method will work the best, as the computer reads through each line it will stack up that information to the very last line, then it can get store it in a reverse order after reading all of them.
2)The list data structure seems to fit this case, making a list of 50 at a time then move on to the next 50.
3)A queue would work best in this situation, you can set thelimit of the queue, read 42 lines into the queue and check if the 43rd one is empty.
4)The USet seems the most appropriate for this problem because it sorts its element. By using sucessor search you can compare one line to the next and end avoid duplicates.
5)The USet would be appropriate for this problem aswell, because the interface sorts its elements you can check and see if the line may be duplicated.
6)Again I would use USet, adding the all the lines while using find(x) to make sure that none are duplicated, afterwards compares the lines one by one to get a sorted list by length.
7)The approach can be the same as the last problem, simply without the find(x)
8)I would read the lines all into a list then create a loop of outputing every other line
9)I would create a list of all the lines... and switch items in the list? I'm not certain if that's possible

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.3
Store the string into a list and then you will be able to compare the opposite if it matches the bracket by dividing by two and add/subtract the value from that element. For example "{[()]}" the [ is the second element out of 6, 6/2 is 3 and the differentbetween 3 and 2 s one therefore add 1 to 3... comparing element 2 and 4. 

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - contents of a file
2. tree - points to blobs... kind of like an address that breaks down (State, city, street, number)
3. commit - saving a blob with changes from the previous one
4. repo - A place to store data
5. hash - A unique identifier for a blob, different for every blob that is different. cannot be manufatured( I cannot get a specific hash I want)