Author
==========
"Zhong, Mingwei", zhongm2
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

My answer: I think it is OK to keep it on USB drive as long as you don't 
loose it or damaging it. But I still wouldn't suggest to use USB because
once you loose or damaging it, you might loose some data of your project which 
you are currently working on. M drive is better because it doesn' make too much sense for me to loose M:drive. HOWEVER, Git will only recognize one computer, 
which means if you switch to another computer, Git will not recognize it. 
For instance, you are working on the lab in Miami University, you put your 
local copy of your repo on M: Drive. You think you finish it and then going 
back home. Suddenly, you realize that you forget to push your project to Github.
The only way you can do in this situation is to go back to the lab,find out
the computer you just using and push it.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

My answer: First of all, you need to use git clone URL command to clone your
repo to the computer and then using git pull command or git fetch command to
get your latest version of work from Github. By the way, I would like to use 
git fetch command because I think it is safer. It allows you to check the 
update information before merging.

#### 3. Morin, Exercise 1.1 (p. 23)
1.My answer:
First of all I want to mention that I migh have some C++ codes below to explain
my strategy, but I use Vim editor so my code might not be compiled. For the
first question, I will first read the txt file each and use STACK to print 
out the content reversely, because Stack is LIFO style. The key code is basicly
like:
stack <char> s;
char a;
while(cin.get(a) && a != '\n')
  s.push(a);   //add the content to the Stack
while( !s.empty() ) {
  cout << s.top();   //from the top
  s.pop();
  }
  cout << '\n';
  }
  
2.My answer:
1.Create a Stack type of string.
2.Read the txt file each line and push each line's content to the
Stack 50 times.
3.Use pop to print out each line reversely .
4.Check if txt file still has next line, if it doese, keep repeating the same
way in order to print out each line in the file reversely.

3.My answer:
1.Create a Queue type of string.
2.Read the file each line and push each line's content to the Queue 42 times.
3.Check if 43th line in the file is empty, if it is empty, print out the
element in the head of the Queue.
4.Read the next line and by using the same way until no more lines in the
file to read.

4.My answer:
1.Create a USet type linked list.
2.Read the txt file each line and use add(x) method to add them in the USet.
3.Print out the content if add(x) return true.
4.Keep reading the file until there is no more lines to read.

5.My answer:
1.Create a USet type linked list.
2.Read the the txt file each line and use add(x) method to add them in the USet.
3.Print out the content if add(x) return FALSE.
4.Keep reading the file until there is no more lines to read.

6.My answer:
1.Create a SSet structure.
2.Read the entire file and store each line in SSet by using add(x) method, at 
the same time use find(x) to ensure there is no duplicated lines in the SSet.
3.Use compare(x,y) method to order the lines with the shortest line first.

7.My answer:
1.Create a SSet structure.
2.Read the entire file and store each line in SSet by using add(x) method.
3.Use compare(x,y) method to order the lines with the shortest line first.

8.My answer:
1.Create a arraylist.
2.Read the file and store each line in the arraylist and record the number of
line in the file.
3.Use a for loop to print out the even numbered lines.

9.My answer:
1.Read the entire file and record the number of line.
2.Create a string array and assign the number of line as its size.
3.Read the file again and store each line of content in the file to array.
4.Generate random numbers to print out the content in the array randomly.



#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

Pick Exercise 1.4:
By solving this problem by using below several steps:
1.Pop all the elements from stack. (LIFO policy)
2.Push the elements to Queue.
3.Finally pop all the elements from Queue. (Queue is FIFO policy) 



#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - Each version of a file is represented as a blob, a contraction of
"binary large object," is a term that's commonly used in computing to refer
to some variable or file that can contain any data and whose internal structure
is ignored by the program. A blob is trated as being opaque. A blob holds a 
file's data but does not contain any metadata about the file or even its name.

2. tree - A tree object represents one level of directory information. 
It records blob identifiers, path names, and a bit of metadata for all the filesin one directory. It can also recursively reference other tree objects and thus
build a complete hierarchy of files and subdirectories.

3. commit - A commit object holds metadata for each change introduced into the 
repository, including the author, committer, commit date, and log message. Each
commit points to a tree object that captures, in one complete snapshot, the 
state of the repository at the time the commit was performed. The initial commit
, or root commit, has no parent. Most commits have one commit parent.

4. repo - A Git repository is simply a database containing all the information
needed to retain and manage the revisions and history of a project. In Git, 
as with most version control systems, a repository retains a complete copy of
the entire project throughout its lifetime.

5. hash - A hash value is a result of a calculation that can be performed on 
a string of text, electronic file or entire hard drives contents. Hash values are used to indentify and filter duplicate files. In Git, hash value can be 
represented the name of a tree, each blob in a tree also has its own hash value,so tree lists files, and points to their blobs according to their hash values.


