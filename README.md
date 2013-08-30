Author
==========
"Luo, Yu", luoy6
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

[No, it is not okay to keep my local copy of repo on a USB drive and just carry it around. It is also not okay to keep it on the M: drive. The reason is because that data on the repo has a greater chance to get lost if I keep my local copy of repo on a USB or M:drive. For example, I could lose my USB drive, and thus losing my whole repo. Miami University may lose my repo my M: drive. Even if Miami University keeps a back up of my M: Drive, it will take a lot of effort to get my data back.]

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

[Every time I do a commit, I will do a push. This way, my repo will be safe and sound at github.com. So if one day I come into the lab and forget to bring my USB drive with my repo, I will just go to github.com and clone one]

#### 3. Morin, Exercise 1.1 (p. 23)

[1. Read the input one line at a time and then write the lines out in reverse order, so that the last input line is printed first, then the second last input line, and so on]
Several interfaces could be used for this, but Deque is the better choice. Since we do not know the total number of lines, any List interface wouldn't be a good choice. If there are n lines, and if we use FILO and LIFO, to read and write n lines, we need to do n * n operations. However, if we use Deque, we only need to do n operations.

	void function reverse
		while the file has next line
			remove last line and add to first line
[2. Read the first 50 lines of input and then write them out in reverse order. Read the next 50 lines and then write them out in reverse order. Do this until there are no more lines left to read, at which point any remaining lines should be output in reverse order]
Since we have a size of 50 lines to work with, it's better to use a List interface, and USet is a better choice here. 


	void function reverse50
		put x(0) in a temporary variable
		for(int i = 1; i<50; i++)
			add x(i) to x(i-1) location
		put x(0) in x(49) position
#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

[Exercise 1.4. Suppose you have a Stack, s, that supports only the push(x) and pop() operations. Show how, using only a FIFO Queue, q, you can reverse the order of all elements in s.]

The Stack, s, is a LIFO Queuing discipline. This means that if I do a pop() operation on s, I will get the last element on the Stack. 
On the contrary, q is a FIFO Queuing discipline. This means that if I do a add(x), where x = the element that is removed by s.  
	
	void function reverse
	while s is not empty
		do pop() operation on s
		do add(x) operation on q, where x = s.pop()


#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A blob is one of the four types of objects in Git. Blob contains the contents of a file. A blob holds a file's data but does not contain any meta-data about the file. 
2. tree - A tree is a type of object in Git. A tree object represents one level of directory information. It records blob identifiers, path names, and a bit of meta-data for all the files in one directory. It can have sub tree objects and thus build a complete hierarchy of files and subdirectories. 
3. commit - A commit is a type of object in Git. A commit object holds meta-data for each change introduced into the repository, including the author, committer, commit date, and log message. Each commit points to a tree object that captures the state of the repository at the time the commit was performed. A commit can have parent commit, and a commit reference back to parent commit 
4. repo - In Git, a repo, or a repository, is a database containing all the information needed to retain and manage the revisions and history of a project. The Git repository retains a complete copy of the entire project throughout its lifetime.
5. hash - In Git, a hash is a 160-bit value that are represented as a 40-digit hexadecimal number. The hash value is used to identify files in Git. The has value is also used to represent the name of each object in Git. Hashes can not be inverted. This means that any tiny change to a file causes the hash to change. Thus, Hashes can be used to check a file's integrity.  