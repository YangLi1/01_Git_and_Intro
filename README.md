Author
==========
"Bailey, Sam", baileys2
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

Based on what I read in the Git book, it would not be a good idea to keep a local copy of my repo on a USB flash drive. Although it is definitely possible to do this, flash drives can very easily be lost, misplaced, or even stolen, and so are not a reliable way to keep possibly important or valuable information. The M: drive is a better alternative than USB flash drives, but still should not be used over something like Github because it would be difficult and tedious to work with Miami to regain your information if something were to happen to it.  Github is definitely the best option because it can easily store large quantities of information and can be accessed from any computer with Internet access.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

If this would ever happen to me, I would ideally go online to Github because the most up-to-date version of my homework should be on that site. However if this is not the case, then I would have to go all the way back to my room, grab the USB drive, and walk all the way back to the lab. To ensure that this doesn't happen again, I would push the version of the assignment to Github.

#### 3. Morin, Exercise 1.1 (p. 23)

1. In this situation I would use a stack interface, which uses the LIFO implementation, as this is pretty much exactly what is asked for in the problem.

2. I would also use a stack interface in this situation, although I would add a couple of other features to it. I would include a simple loop to the program with a counter that (when the counter reached 50) would cause the program to stop reading lines of information in and begin outputting them according to the LIFO method instead. Once all of the lines stored were output, the program would begin reading lines in again, and this process would repeat until there was no more information to read in.

3. A queue would be the best way to approach this problem. The program would begin by reading in sections of the file (43 lines at a time), checking for blank lines. If any blank lines did occur, it would be easy to replace them with the earlier line specified in the instructions because it would be the first line in the queue up for deletion (due to the FIFO nature of the interface). Once the queue is filled with information, the oldest line would be deleted and the newest line would be put in, which is not a problem because the oldest line would no longer be needed to possibly replace a blank line.

4. A USet would be the best interface in this situation, as USet does not permit duplicate items. The program I would make for this would read each line in a file and, before deciding whether or not to add it, use the find(x) function to determine if the line has already been used or not. If it has not been used then it would be added, however if it had already been used earlier in the file it would not be added.

5. this would be another instance in which a USet would be used, for the same reasons as the previous situation. I would also use a List in this problem. 

6. An SSet should be used in this in order to print all of the lines by length. I would use the compare(x,y) function to sort the lines, and I would use the find(x) function to locate any duplicates and then remove them.

7. This problem is very similar to the last one in many ways, so an SSet should also be used here. I would use the compare(x,y) function again to sort through the lines in the file. There would be no need to check for duplicates, however, as they are allowed in this situation.

8. In my opinion a list interface should be used here due to the fact that the lines of the file do not need to be ordered in any way. The lines in the file would be read into the list, and then I would utilize a loop and the get(i) function to output the even elements, then output all of the remaining odd elements.

9. A list should be used here.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.2  There are multiple relationshops between Dyck words and the aforementioned Stack operations. Stack push(x) and pop() operations, like Dyck words, cannot have negative sequences of 1's, both + and -. For all intensive purposes the methods of push(x) are the same as a +1 in a Dyck word, while a -1 is very similar to a -1. 

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A blob is basically all of the contents of a given file in a git repo. It ONLY holds the content of the file, not the file's name or any metadata pertaining to it.
2. tree - A tree is essentially the directory for a given repo. It contains metadata, any identifiers, and the location of the repo.
3. commit - A commit holds the metadata for each individual change in a repo. They also point to other objects such as trees.
4. repo - A repository; the place where all of the information needed to manage and edit a project are held, as well as the project's history.
5. hash - the hex representation of a file; essentially the unique label that is used to identify a specific file.