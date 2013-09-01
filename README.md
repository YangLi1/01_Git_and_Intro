Author
==========
"Blase, Douglas", blasedd
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

Based on the reading, it is not okay to keep your local copy of your repo on a USB drive because it is just as prone to failure as a computer is. Once the USB drive fails, the data is lost and cannot be recovered. In addition, you must always have the USB drive with you in order to access your local repo, which is not an ideal situation.

When it comes to the M: drive here at Miami, it is certainly a better option than the USB drive, since the M: drives are backed up periodically and can be accessed from on/off campus, but that still depends on the ability of your computer to successfully establish a remote connection with the Miami servers, and that may be unreliable at times. The best option is an online server, such as github.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

If the repo was also up to date online on github, then I would clone the repo to the computer at the lab. 

If that isn't the case, then you should go back to your room and get the usb drive, and subsequently (or before you return to the lab) push your repo to your online server so the issue doesn't happen again.

#### 3. Morin, Exercise 1.1 (p. 23)

1. A stack would be the best interface to use in this scenario, since that uses the "Last in, First Out" (LIFO) implementation, which is exactly what is asked for in the description.

2. Just as in 1., I would use a Stack to accomplish the task, but to ensure that the whole file is not read in and then out put, I would use a counter to keep track of how many lines have been read in. Once the counter reaches 50, I would stop the program from reading in more lines and instead begin outputting the lines in LIFO order. I would use a while loop that keeps repeating this process until there is nothing left to read in the file.

3. To accomplish the task of reading 42 lines, and then following those 42 lines, checking for an empty line and then printing the line that occurred 42 lines prior to the blank line, a queue that stores a maximum of 43 lines of text would be required. The queue would be the best option because once the 44th line would be read, it would replace the very first line that was read by the program, which is acceptable because the first line isn't needed anymore. When a blank line would be encountered, it would be easy to access the line of text that was located 42 lines prior to it because it would be the first element to be deleted from the queue due to its "first in, first out" structure.

4. For a program that would only print a line of text that is not a duplicate, I would recommend using an SSet because it is an ordered set. I would first store each occurrence of a line in the SSet in alphabetical order (since we're using a text file). After reading in a line, I would compare the line to the contents of the SSet. If a match isn't found, I would store the line in the SSet and then output the line. If a match was found, I would not store the line, nor would I output it.

5. For similar reasons to 1.1.4, I would use an SSet again. In this case, the first occurrence of each line is still stored in the ordered set. When a match IS found, I would replace the line in the SSet with the line that was just read in, and I would then print that line.

6. To print all of the lines sorted in order by length (shortest to longest), I would use an SSet. I would configure the SSet to store the lines in order of length (shortest to longest), and then have it break ties by sorting the sentence alphabetically. Before storing the line in the set, I would check to see if there was a duplicate line already in the set, in which case I would not store the duplicate line. Once all of the lines have been read in, I would print the lines from the SSet, starting from the first index of the SSet and ending at the last index of the SSet.


7. My approach to this question is exactly the same as the approach to my answer to 1.1.6, with the only change being that I would not check for duplicate lines, since all duplicate lines are to be printed.

8. A List would be the best interface to use in this instance because the lines do not need to be ordered. Once all of the lines were read in to the List, I would use two loops to print the text. The first loop would start at the very first line (index 0) and print every other line until the end of the List is reached. Once that loop has completed, a loop that starts at index 1 and prints every other line would be used.

9. Ideally, I would use the List interface to accomplish the task of printing the lines in any order because they are the easiest to shuffle the contents. After the contents have been shuffled, I would then just print the lines starting from the beginning of the list and ending at the end of the list.


#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.4 - To reverse the elements in Stack s with a FIFO Queue q, the following would need to be done. The contents of s would need to be popped to the FIFO Queue q. Due to the LIFO nature of s, its elements would be removed in the reverse order that they were pushed to the stack. Since q is a FIFO q, removing the elements from q and pushing them to s would put the elements in s in the same order as they were in q, thereby reversing the order of the elements as they were originally ordered in s.

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A blob is essentially a file in a git repository, such as the README.md file. This is how git represents a file.
2. tree - The directory for the repo, the tree contains identifiers, the location, and metadata for the repo.
3. commit - Commits hold the metadata for changes made to files in the repository. Commits make the changes permanent.
4. repo - The outer database (think of it like a container) that contains all of the trees, blobs and anything else related to git.
5. hash - The unique identifier of each file that is part of the git repository.