Author
==========
"Mullins, Harrison", mullingh
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

I do not believe it is okay to keep the local repository on a USB drive.  Unless it is a clone of the original, I think the USB should solely be used for cloned repositories.  Because a USB stick can easily be lost, then you would not have the local copy of the repository any more.  The M:Drive is more acceptable than a USB stick, but again it should be used for cloning purposes not for keeping the original local copy of the repository.  Because the M : drive is subject to changes, and our restricted access doesn't allow us to do all the operations that may be necessary.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Clone my repo from github and create a new branch off of the repository.  Then when I have my USB again I can merge the branch with the master branch on my local repository and commit the changes.

#### 3. Morin, Exercise 1.1 (p. 23)

1. I would use just only a stack to accomplish this, and push every element in, then pop out every element accordingly.
2. This problem can be solved using a stack again with some simple constraints and while loops. Once the stack has reached the limit of 50, it will print the first element on the stack in reverse order until the stack is empty, then repeat the process.

Pseudo-code:
while(hasNextLine == true) {
	int count = 0;
	stack s;
	while(count < 50) {
		s.push(nextLine);
		count++;
	}
	while(s != null) {
		println(s.pop());
	}
}
3. I'm not sure how to code this into pseudo-code but I would use the FIFO queue structure to solve this problem. I would have a queue of size 43 where it would add an element until the queue reaches the size of 43, then after that point every time a new element is added it would remove the first element in the queue.  Upon reaching a blank line or element it would print the first element in the queue. All of this would happen until there are no more lines to be read.
4. I would use a USet data structure and use the find(x) function to check if the element is present already in the set.
5. I would again use the USet data structure and use the find(x) function to check if the element is present already in the set. If the element is present a second time I would then print the output and remove the first occurrence of the element from the set using remove(x).
6. I would use the SSet data structure using the find(x) to find the smallest lengths of elements in the set to sort it, then use compare(x,y) to check if the elements are the same length. If the elements are the same length and compare returns true, then it will only print once and skip the next entry.
7. I would do the same as the previous question yet I won't skip duplicate entries.
8. I would use two FIFO queues for this.  I would first read in the entire input one line at a time into a FIFO queue, then I would print each even element starting with 0, and on every odd element add it to the other empty FIFO queue(while removing each element after it has been printed).  After the first queue is empty and all the even elements have been printed, the second queue would simply print each element in its queue(while removing each element after its printed).
9. The only way I can think to do this currently using only the data structures given is to put all of the elements into a stack, then pop them into a queue of varying size, then return the elements into the stack.  And then repeat this process a couple times to "randomize" the order, then just print the elements off the top of the stack.



#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

1.4
In order to reverse the elements of a stack s, using only the push(x) and pop(), along with the FIFO queue q, I would use the following.  First I would pop() all of the elements from s and add them to the queue one by one until s is empty. Next, I would remove the elements from the queue and push them to the stack one by one until the queue is empty.  The elements in s would now be reversed.
In pseudo-code it would look like the following:

while(s != null)
	q.add(s.pop());
while(q != null)
	s.push(q.remove());

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - The data stored in each version of a file is a "blob" or a binary large object.  So each time we create a new commit of a file, a blob is created to store that version of the file.
2. tree - A tree is a directory that contains the data related to all the files on that level.  It contains the structure of repositories and their files so that they can have a hierarchy of all the directories.
3. commit - A commit is an object that holds the data necessary for each change introduced to a repository.  This includes the author, committer, commit date, and log message.  Commits reference a tree object in order to update the state of the repository at that time.
4. repo - A repository is a database containing all the information in regards to all the files related to a project, and all the revisions related to those files.  Specifically a git repository contains all the working files in a repository but also a copy of the repository itself.
5. hash - A hash is a unique identifier for an object and can be used to refer to that object after the hash function has created the identifier.  It is used for both security reasons and performance reasons and allows git to give each version a unique identifier to be tracked by.  Statistically no two files or versions should ever have the same hash value, although in theory collisions may occur.