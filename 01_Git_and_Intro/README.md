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

No, you should not carry your repo on a USB drive and just carry it around.  By using Github to save your file, you eliminate the chance that losing your USB drive will also lose your entire repo.  Using Github also allows you to access your repo from any computer without having to carry a storage device, and risk losing your data.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

You should clone your repo from Github to the local computer you're on. After working with your repo and committing your work, you should send a pull request to your remote repo on Github so that you can keep your work all together in your project repo.

#### 3. Morin, Exercise 1.1 (p. 23)

	1. I would use a LIFO queue for this task.  Once you reach the end of the lines, the last line read in would be the first one you want to print when printing in reverse order.
	2. I would continue to use a LIFO queue for this task.  With the same goal, specify to read 50 lines of a document, print them in LIFO order, then read the next 50 lines and continue.
	3. For this task I would use a list structure.  Once you reach a blank line after line 42, the first element in your list at the time will be the line you want to print (42 lines before you reach the blank one).  You would have to shift your list each time you read a line to be sure not to store over 42 lines at once.
	4. I would use a USet structure. As you read new lines, check against a created stored set to see if they have already been added.  If so, skip that line. If not, add that line to the set and print it in the output.
	5. Continue to use the USet structure.  As you read lines, add them to the set. Once you come across a line that is already in the set, print it to the output without adding it to the set again.
	6. I would use a priority queue.  After reading in all lines, remove and print to the output the smallest lines that have been read in.  If lines are duplicates, print to the output only once.  If lines are the same length, use the usual "sorted order" for whatever type of data you are reading in.
	7. For duplicate lines, print the line once for each time it was read in.  You will have an output that is the same number of lines as the input you read in.
	8. I would use a list structure.  After reading the entire document, print to the output the lines that were indexed with even numbers.
	9. I would use a list structure for this also.  It is the only alternative that allows you to have all lines stored, use index numbers to access any line at will (not stacked), and print them randomly.  Use a randomizing function to select an index number from the list, print the line on the random index position, remove that line from your list, then select a new index randomly, etc. 

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.4
	To complete this task, you would pop() all the elements from the stack, starting at the top and working all the way down.  Adding these elements to a FIFO queue will in essence reverse their order, since the last element read into q will be the first one out of q.  Once all the elements are moved from s to q, you'll push the elements back to s, which will have reversed their original order by the nature of a FIFO queue.
ex. 	q.add(s.pop(3));
	q.add(s.pop(2));
	q.add(s.pop(1));
	q.add(s.pop(0));

	s.push(q.at(3));
	s.push(q.at(2));
	s.push(q.at(1));
	s.push(q.at(0));

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - the immutable contents of a file. Contains no metadata
2. tree - one level of directory info that records blob id's, pathnames, and metadata
3. commit - an object that snapshots the tree metadata and the state of a repository at the time the commit object is created
4. repo - a database that contains all the revision history of a project, as well as a copy of itself to work from.
5. hash - a unique code assigned to an object based on it's contents.  If two objects are duplicates or exactly the same, they should always have the same hash code, no matter on what computer or system, if git is being used.
