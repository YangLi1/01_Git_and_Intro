Author
==========
"Stilgenbauer, Kendall", stilgeki
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

Since Git was made to support distributed development, you could keep your repo on a flash drive or the M: drive, yes.  It should be fully functional on any computer with Git.  A better method, of course, would be to use Github and clone the repo onto whatever unfamiliar computer you're using.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

You should clone the repository from Github, and go about your work as normal.  Easy facilitation of distributed development is one of the best things about Git and Github.

#### 3. Morin, Exercise 1.1 (p. 23)

1. This can be accomplished by reading each line into a Stack, and then removing and printing each line.  Since Stacks use LIFO, the input will be reversed.
2. This time, instead of reading in the entire file, a loop merely reads in 50 lines at a time, putting each line into a Stack.  It then prints each of those lines from the Stack.  Next, it moves on to the next 50 lines in the file and so on.  Each set of 50 lines will be reversed because Stacks utilize the LIFO queueing discipline.  If there aren't 50 lines remaining, it will fill the Stack with however many lines are remaining.
3. I would implement a FIFO Queue.  I would initially read the first 42 lines into the Queue without checking anything.  For every line after that, if it is blank, I would removeFirst() and print it.  If the line is not blank, then the first item in the Queue would only be removed.  A Queue is used instead of a Stack, as in the previous parts, because Queues are FIFO.  This is important so that the correct line is removed and printed in the case of a blank line.  A LIFO Stack would merely print a blank line, or the 42nd element of the Stack, depending on whether the line is checked before or after it is put into the Stack.
4. A USet is the order of the day here.  As each line is read in, it should be added to the USet.  The USet.add(x) method automatically checks if the line is a duplicate or not.  If it returns true (the line was added to the USet), the line is unique and should be printed.  If it returns false (the line was not added to the USet), the line is a duplicate and should be discarded.  This has the dual functions of checking for duplicates so they don't get printed and not taking up memory with duplicates, as a List would do (a List was my first thought for this problem).
5. This problem is very similar to problem 4.  You still implement a USet and check the value returned by the USet.add(x) method, but this time the line is only printed if the value returned is false.
6. First, the entire input should be read into an SSet.  This will remove the duplicates and sort the lines by their length.  Then, the elements of the SSet should be printed.
7. I don't think my solution for this one is ideal (it seems rather clunky), but it is the best I could come up with.  Each line of input should be read into an SSet.  If it cannot be added (because it's a duplicate), it is instead added to a List to keep track of it.  When all of the input has been read into either the SSet or the List, the unique lines will be sorted.  They are then added to a new List in their sorted order.  Then, each element in List 1 is checked against the elements of List 2.  When a match is found, the element from List 1 is added to List 2 immediately following the one it matched, to retain sorted order.  This continues until all the duplicates have been added back in.  Then, List 2 is printed out.  I feel like there HAS to be a better way to do this, but that's what I came up with.
8. The input should be read into a List.  Then, a loop should iterate through the elements of the List, starting with i = 0, printing the line, and incrementing twice (to the next even number).  Then a second loop should iterate through the list starting at i = 1 and performing the same actions.  A List is used so the element numbers can be referenced for ease of printing the even-numbered or odd-numbered lines.
9. The entire input should first be read into a List.  Here again, the List's ability to access any of its elements by their index is necessary.  A random index number is chosen by a random number generator.  Then a loop is initiated that prints the index and removes it from the List to prevent printing the same line again.  To continue the loop, a new index number is randomly generated.  In this way, the entire collection of lines is output in a random order.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

Exercise 1.4: This problem is fairly simple, in practice.  To begin, we need to push(x) every element we want to be in Stack s.  Then, we pop() them all out and enqueue(x) them in our FIFO Queue, q.  After every element of s has been transferred to q, we then perform the dequeue() function on each and push(x) it back into s.  The elements of s will be reversed.  For example, say we're dealing with the numbers 0 through 9.  We start with the contents of s as such: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9.  Since 9 was our Last In, it is the First Out and the First In for q.  After the full transfer, the elements of q, from first to last, will be 9, 8, 7, 6, 5, 4, 3, 2, 1, 0.  9 was the First In, and so it is the First Out for q, and it is pushed back into s, followed by the others, so the final order of s is: 9, 8, 7, 6, 5, 4, 3, 2, 1, 0.  As promised, this is the reverse of the original order of the elements of s.

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A blob contains the contents of a file, but no other information about it, even the file's name.  The blob also doesn't care about what kind of file it is.
2. tree - A tree is sort of like a folder, in the respect that it contains one or more blobs or sub-trees, with metadata and path names to access these blobs and sub-trees.
3. commit - A commit object represents a specific version of a repository.  It holds information like the author, commiter, time of commit, and a user-defined log message.  It points to a tree that holds the information that was in the repository at the time of the commit.
4. repo - A repository is a container for each version of a project.  It contains a complete copy of the project and past iterations of the same project.
5. hash - A hash is a globally-unique identifier for a git object.  It is represented by a 40-digit hexadecimal number, but can be referenced by the first 9 digits for convenience.  Hashes are created by the SHA1 algorithm, and are unique to the content in a file.  It is effectively impossible for the same hash to be generated for different files, so a hash is as good an identifier for an object as fingerprints and retinas are for humans.