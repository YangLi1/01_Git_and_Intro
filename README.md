Author
==========
"Proctor, Patrick", proctopj
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

If it's your only local copy, no, keeping it on a USB drive is not kosher due to risk of loss/theft; however, keeping "A" copy is useful if one must change venues often as long as it remains updated
and is eventually brought back to your primary computer. The M: drive is not a good location to keep one's repository due to the multitude of people who have access to it which are not affiliated with
your projects who could steal or damage the data. While keeping a backup repository could be seen as protection by redundancy, I personally would not risk that much data exposure. In fact I do not 
connect to the internet on the computer where I store most of my coding projects because on the internet privacy is a fantasy.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

Go back to the dorm and get the USB... If you were smart and pushed an up-to-date repository onto 'github' or another accessible site, simply clone or otherwise download the repository from there.

#### 3. Morin, Exercise 1.1 (p. 23)

1)Using an ArrayStack structure, read in each individual line of the text file in order until no more lines remain (Java's hasNextLine() being a handy tool to avoid an IOException), add them to the stack, then remove (write) them. 
The remove() method automatically removes the final (top) element of the ArrayStack, so the inherrent simplicity lends itself to a speedy operation  as well as a very simple code implementation.

2)Using the same overarching principle as in 1.1_1, this time include a loop structure of choice to track the number of elements added into the ArrayStack. While the ArrayStack has less than fifty elements, if the file has more 
lines to be read, add them to the stack until it has exactly fifty elements. At this point (or if no lines remain) remove and print the stack elements to produce the fifty lines in reverse (50-1,100-51, etc.).

3)Using an ArrayDeque (due to quick access to both ends of the "list"), implement a while loop which always checks for more lines in the file, and inside use an if-statement which checks the number of elements currently in the 
ArrayDeque (for our purposes, a limit of 43 seems logical). While the number of elements is less than 43, continue reading in more lines from the file. If a blank line appears before 43 elements fill the ArrayDeque, add it to 
the ArrayDeque and continue to 43 elements. After 43 elements have been accrued, each time a new line is read, the "first" element of the ArrayDeque is removed, regardless of whether or not the read line is an empty string. 
If the read string is empty, the removed element is displayed.

4)Using an ArrayStack (or any other quickly searchable data structure) as each line is read in, have it checked against current elements in the ArrayStack. If it already exists in the Stack, move onto the next line. If it does not,
add it to the Stack and send it to the output.

5)Using the same principle as 1.1_4, instead of sending lines to output when they do not already exist in the stack, send them only when they DO already exist in the Stack.

6)This problem is a bit more complicated. Whether it is more efficient to sort the Array as each new element is added and then search or to search for each element and then sort once at the end is not entirely clear. For the sake of
simplicity, I will choose to sort only once. As each line is read in, it will be checked against the Array to see if a duplicate already exists. If a duplicate exists, the line is not added and the program continues to the next line.
While the complexity of the duplicate search grows as the list grows, it is difficult to say whether this is more or less efficient than sorting by length and searching by length for each new entry. When all lines have been read, sort
the entries by length and then by alphabetical order for entries of the same length. This is most quickly done by an iterative, multithreaded implementation of the QuickSort or Quick3 algorithm so that the least elements are at the 
top of the Array. At this point, remove each element and send it to the output.

7)Apply all the same ideas in 1.1_6 except add a variable to each Stack entry including the number of times the element has appeared in the read-in (simply add a new function which iterates the variable by one for each subsequent 
appearance). When it comes time to output the entries, use a loop to iterate the printing via this new variable.

8)Read all lines into an Array and then simply get/output the even numbered lines via a +2 iterated loop, subtract n-1 elements from the loop control variable, and then get/output the odd-numbered lines.

9)Read in all lines to an Array. At this point, implement a decrementing for/while loop with the control variable being a value size-1 in terms of the Stack size. Inside the loop, employ a RNG to remove a "random" element from the 
Array --ex: get/remove(random()*(size-1))-- NOTE: the text is not totally clear on whether or not the list interface remove(i) method returns the value at Xi or not. If it does not, then inside the loop a variable would store the generated
number and apply it to both methods get(i)/remove(i). Not being completely familiar with RNG and their operational time, I'm not sure if this path or randomizing the list itself and outputting in order would be more efficient. I find this
method more creative.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Exercise 1.2) In simple terms, a Dyck Word is a binary function whose prefix cannot be negative. If the current total sum of -1s and +1s is greater than -1, pushing a new element will generate a new dyck word regardless of whether the element
is positive or negative. If the current total sum is negative, the contrapositive is true, and a Dyck word cannot be generated regardless. Popping off elements can generate new Dyck words if the current total sum is -1 or greater and the 
removed element is -1. In a way this is how bits arrange to form our basic data types like int, short, byte, ubyte, etc.... Although, bits can never be negative so there is no "invalid data type" generated by their designation as 1s and 0s.

#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - A generic git data structure with holds information about the data it contains, but does not actually show the data. A blob can contain a file, another data structure, or almost anything really except higher git data structures, such
          repositories and trees.

2. tree - A simplified implementation of UNIX directories to include branches and store the blobs within those branches. The trees contain file pointers (somewhat like mini hash values which denote file/blob types) and hash values for each file.
          Trees can also link to other trees for certain project paradigms.

3. commit - A command which takes the changes in a user's directory and implements them in the git repository. The commit also generates a new unique version of the repository (by way of highlighting the differences to use as little memory as possible)
            while leaving the previous repository alone. This is the essence of the version control. Commits also come with a description feature which allows one to say what was changed between commits.

4. repo - Short for repository, a git repo is a structure by which git stores files and information. It comes formatted in such a way git can quickly define differences between a repo and a directory or between two repos. Repos are linked to branches in
          a project (in classical use) but can be created on their own should the user desire to use the structure for version control on a small, independent work.

5. hash - A unique alphanumeric string (limited to hex values) which is generated to describe a file in shorthand. Git uses these as markers to access previous versions of files and compare files as well. Though two different files could arrive at the same
          hash value, the chance of it occurring is almost entirely negligible. The tiniest edit of a file will generate a new hash value.