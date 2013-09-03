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

No, it is not okay to keep my local copy of repo on a USB drive and just carry it around. It is also not okay to keep it on the M: drive. The reason is because that data on the repo has a greater chance to get lost if I keep my local copy of repo on a USB or M:drive. For example, I could lose my USB drive, and thus losing my whole repo. Miami University may lose my repo my M: drive. Even if Miami University keeps a back up of my M: Drive, it will take a lot of efforts to get my data back.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Every time I do a commit, I will do a push. This way, my repo will be safe and sound on github.com. So if one day I come into the lab and forget to bring my USB drive with my repo, I will just go to github.com and clone one.

#### 3. Morin, Exercise 1.1 (p. 23)

[1. Read the input one line at a time and then write the lines out in reverse order, so that the last input line is printed first, then the second last input line, and so on]

Here, Stack is a better choice. A Stack process the lines on a last in first out (LIFO) basis, so when we read a line, and put it on a Stack, the first line will be on the bottom of the Stack, and the last line will be on the top of the Stack. So the lines will be in reverse order after we put them on the Stack. Since this process only requires one operation on each line, that is, read one line at a time and put it onto a stack, it should be fairly fast.

	function void reverse
		while there are more lines
			read one line and put it on the Stack
		print out the Stack

[2. Read the first 50 lines of input and then write them out in reverse order. Read the next 50 lines and then write them out in reverse order. Do this until there are no more lines left to read, at which point any remaining lines should be output in reverse order]

Similar to problem 1, a Stack is a good choice for this problem. Instead of reading one line at a time, we read the first 50 lines one line at a time, and we put the first 50 lines onto the Stack. We then read the next 50 lines (from line 51 to 100) one line at a time, and we put them onto the Stack. This will reverse lines as the question asked us to do, and by doing this, we never have to store more than 50 lines at any give time.


	function void reverse50
		while there are 50 lines
			read the 50 lines one line at a time and put them onto the Stack
				print the Stack
		read the left lines that are less than 50 lines, and put these lines on the Stack
			print the Stack
			
[3. Read the input one line at the time. At any point after reading the first 42 lines, if some line is blank, then output the line that occurred 42 lines prior to that one]

Here, A Queue is a better choice. A Queue process the lines on a first in first out (FIFO) basis. When we read the first line and put it on the Queue, it will appear on the top of the Queue. When we read the last line and put it on the Queue, it will appear on the bottom of the Queue. So if we read a blank line at Line 43, then the line that occurred 42 lines prior to Line 43 is Line 1, then we could just print the first line on the Queue. Once we print the first line, we remove the first line from the Queue and read the next line. If Line 43 is not a blank line, we simply remove Line 1 and read the next line. By doing this, we never stores more than 43 lines of the input at any given time, thus this should be a fairly fast process.

	function void never43
		read the first 42 lines and put them on the Queue
		while there are still lines in the file
			read the next line
				if the next line is blank
					print Line 1 on the Queue, and then remove Line 1 on the Queue
				else
					remove Line 1 one the Queue
		
[4. Read the input one line at a time and write each line to the output if it is not a duplicate of some previous input line.]

In order to find out whether or not a line is unique, both USet and SSet require comparisons. But if we use SSet, we could sort the lines. Once they are in order, we can remove the duplicated lines by comparing neighbouring lines. Since we only need to compare two lines at a time, this should be a faster process than using USet. 
	

	function void notDuplicatedLines
		sort all the lines and put into a set s 
			for(int i =0; i< s.size-2, i++)
				compare whether two lines are equal (duplicated) by comparing s(i) and s(i+1)
				if the two lines are duplicated
					remove one of them
		print set s
		

[5. Read the input one line at a time and write each line to the output only if you have already read this line before]

Here, a USet is a better choice. If we use SSet, after we sort the lines, we have to do at least two comparisons to a line (comparing a line to the line before and the line after) to find out whether or not it is a unique line. A USet contains n distinct elements; no element appears more than once. Thus, we could put all the distinct elements in the USet, and remove the entire USet in the end. This will leave duplicate lines in the file, and we just print them out. Using USet, we do not have to store a lot of duplicate lines in the USet. So if a file with a lot of duplicate lines does not use more memory than what is required for the number of unique lines. Thus using USet should be faster than using SSet.

	function void duplicatedLines
		read the lines and put unique lines into USet s
		remove s

[6. Read the entire input one line at at time. Then output all lines sorted by length, with the shortest lines first. ]

Here, order is important because we want to sort the lines by length. Thus, a SSet is a better choice. 

	function void sortByLength
		sort all the lines by length and put into a set s
			while the file still has lines left
				compare two lines at a time
					if two lines has the same length and the same contents (duplicated)
						remove one of them
					else
						print the first line
			advance to the next line
				
[7. Do the same as the previous question except that duplicate lines should be printed the same number of times that they appear in the input. ]

Same as problem 6, order is important here. Thus, SSet is a better choice. We read the file and sorted the lines by length. In the end, we print out the whole set as it is. 

	function void sortByLength2
		sort all the lines by length and put into a set s
		print set s

[8. Read the entire input one line at a time and then output the even numbered lines followed by the odd-numbered lines]

Here, we can implement a DeQue. We read through the lines, if it is odd numbered line, we add it to the end of the Queue. If it is even numbered line, we add it to the beginning of the Queue. Using a DeQue, we only need to read through the lines one time. Thus, it should be faster than using Queue or Stack

	function void evenOdd
		while there are lines in the file
			read the next line
				if it is even numbered line
					add to the beginning of the Queue
				else
					add to the end of the Queue

[9. Read the entire input one line at a time and randomly permute the lines before outputting them]

Implements a SSet. After reading through the lines and put them into a sorted set s, we then randomly swap the lines in the set. Finally we print out the whole set s. Since USet only store distinct elements, it might be faster using SSet.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

[Exercise 1.4. Suppose you have a Stack, s, that supports only the push(x) and pop() operations. Show how, using only a FIFO Queue, q, you can reverse the order of all elements in s.]

The Stack, s, is a LIFO Queuing discipline. With a FIFO Queue, q, we can easily reverse the order of all elements by simply read the Stack and add to the Queue. 

	function void reverseS
		while there are still elements in the Stack s
			read the Stack s and do a pop() operation on the first element
			put the first element in the Stack s into a Queue, q. 


#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A blob is one of the four types of object in Git. Blob contains the contents of a file. A blob holds a file's data but does not contain any meta-data about the file. 
2. tree - A tree is a type of object in Git. A tree object represents one level of directory information. It records blob identifiers, path names, and a bit of meta-data for all the files in one directory. It can have sub tree objects and thus build a complete hierarchy of files and subdirectories. 
3. commit - A commit is a type of object in Git. A commit object holds meta-data for each change introduced into the repository, including the author, committer, commit date, and log message. Each commit points to a tree object that captures the state of the repository at the time the commit was performed. A commit can have parent commit, and a commit reference back to its parent commit 
4. repo - In Git, a repo, or a repository, is a database containing all the information needed to retain and manage the revisions and history of a project. The Git repository retains a complete copy of the entire project throughout its lifetime.
5. hash - In Git, a hash is a 160-bit value that are represented as a 40-digit hexadecimal number. The hash value is used to identify files in Git. The hash value is also used to represent the name of each object in Git. Hashes can not be inverted. This means that any tiny change to a file causes the hash to change. Thus, Hashes can be used to check a file's integrity.  