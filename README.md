Author
==========
"Bickley, Daniel", bickledb
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

While in theory you can keep a local copy of your repo on a USB drive, it is an inefficient way to work. Additional redundancy is always a good thing, but in this case, it is highly unnecessary. Due to the nature of Git, you do not need to 
bring a USB drive around with you wherever you go. Using Git, you can easily clone the repo and have it at any computer, with any and all changes you have pushed onto the remote server. Having a copy on the USB requires more effort and can actually cause changes that have been made revert to an earlier state. That being said, the greater number of redundant systems, the less likely failure will occur. There will always be scenarios where having a repo on a USB drive can be useful, but they are few and far between. Without a doubt, the USB drive 
should not be a primary tool for storing your data, but if you cannot access the internet at a particular place, then it is better than only using Git. I would also hesitate to put the repo on the M: drive, because it takes a much longer time to access the M: drive and download the repo, which is terribly inefficient.
But again, another form of redundancy is not a bad thing, but the M: drive can be difficult to use and is more inefficient than Git when it comes to time and possible confusion of which is the newest copy.

#### 2. Imagine that you come into the lab on the weekend to work on homework with friends, but you forgot to bring your USB drive with your repo on it. What should you do?

You should simply clone the repo on one of the lab computers. This is the best solution, because of the remote nature of Git. Because Git keeps all of the changes as well as the current copy of the file, you can easily download the newest copy, but be sure to push
 it back to the remote server whenever you stop working, if not more frequently. 

#### 3. Morin, Exercise 1.1 (p. 23)

1.1 Using a LIFO queue, you use a loop that reads in all of the lines of input starting at 0 and continuing until there is no other unread lines, utilizing the add(x) method to add each input into the queue. Then, you can use the remove() method to take out and read the most recently read input, which will be the last input, then second to last, ad infinitum until there are no other inputs left.

1.2 I would begin with using a stack. I would begin with a method with an integer variable, called index. Then,there would be an if statement where if the total number of inputs minus the index variable is less than 50 ,then the method would simply read them in, and then utilize remove() to read the most recent input, followed by the penultimate, so on and so forth, followed by a return statement to exit the method.
If there was more than 50 lines left, I would write the next 50 lines in, incrementing the index variable by 1 each time, until I have read in 50. Then, using the remove() method, they would be printed and taken out. This will be followed by a recursive call to the method.

1.3 I would start with a FIFO Queue with 43 slots.. As input is read into the queue, they are added in using the add(x) method. After the queue reaches a size of 42, the next input is checked to see if it is blank, and then added to the queue. If it is blank, then the input in slot 43 is selected as an output, and is subsequently removed with the remove() method. 

1.4 I would start with a List data structure. The method begins with an initial Boolean variable called “found”, initially set to false.. While the program reads in input using a loop, it checks to see if the input has been read into before by utilizing a loop and the get(t) method, and if it is found, the “found” variable is set to true. If “found” is false, then the input is written to the output, and then added using the add(input,0) method to the List. If “found” is true, then nothing is done with it, and the program proceeds to the next line. When there is no more unread input, the program terminates.

1.5 I would start with a List data structure. The method begins with an initial Boolean variable called “found”, initially set to false.. While the program reads in input using a loop, it checks to see if the input has been read into before by utilizing a loop and the get(t) method, and if it is found, the “found” variable is set to true. If “found” is false, then the input is  added to the List using the add(input,0) method. If “found” is true, then the input is written to the output. When there is no more unread input.

1.6 The data is best organized as a Sset data structure. A loop runs adds each line of input in to the Sset, and follows the following pattern. As inputs are added, the correct placement for each one is found using the find(input) method. If the find(input) method returns any integer except null, the input is compared with the data in the set at slot named by the find(input) method using the compare(input, dataInSlotNumber). If the compare(input, dataInSlotNumber) returns 0, the program skips ahead to the next iteration of the loop. However, if the compare(input, dataInSlotNumber) does not return 0,the input is added at the number the find(input) method returned. If find(input) returned null, the input is added at the end of the Sorted Set. After all of the inputs have been read in, the program runs a loop that prints each line out, starting from index 0 and continuing on until there are no unread inputs. The program then stops.

1.7 The data is best organized as a Sset data structure. A loop runs adds each line of input in to the Sset, and follows the following pattern.  As inputs are added, the correct placement for each one is found using the find(input) method. If the find(input) method returns any integer except null, the input is compared with the data in the set at slot named by the find(input) method. If find(input) returned null, the input is added at the end of the Sorted Set. After all of the inputs have been read in, the program runs a loop that prints each line out, starting from index 0 and continuing on until there are no unread inputs. The program then stops.

1.8 The data would be organized in a List, with a simple while loop reading all of the inputs in using the add(x) method. Then, a loop would run through the List, and if the indexes are even numbers or 0, then they are printed.

1.9 The data would be organized in a List. Using a combination of the get(i) , set(i,x) commands, and a random number generator, a loop goes down the list, randomly generates a number for each index, that is less than the size of the list, and uses the get(i) and set(i) methods to mix the locations of the information around. This loop is done multiple times to generate as much randomness as possible. Then, a simple loop reads down the array and prints the information out in order.

#### 4. Your choice: Morin, Exercise 1.2, 1.3, or 1.4 (pick one)

Note: You should not need to write any real computer code for any of these. Instead, explain how you would approach the problem using a combination of English and pseudocode. The goal is to write something that is understandable by any programmer, even if the two of you have never used the same computer language. (In other words, assume the other person does not know the syntax of Java or C/C++, but knows the basic programming constructs such as for loops, if statements, variables, and so on.)

Exercise 1.2
	Stacks share the same properties as Dyck words because neither can have a negative sequence of +1s or -1s. The push() methods of stacks is equivalent to a +1 in a Dyck word, and the pop() method is equivalent to a -1. In a Stack, you can never have more pops than pushes in any situation because eventually there will be no inputs left in the Stack to pop. In Dyck words, the sum of the prefix cannot be negative, similarly to how Stacks cannot have more pops than pushes. 



#### 5. Define/explain each of the following terms, as they relate to git.

1. blob - The meat of a file, but does not have any defining features, save for a hash code that allows it to be identified. They can contain the contents of any kind of file, and are saved as binary objects.
2. tree - The Git object that holds blobs together, holding the hash codes for specific blobs,  and provide organization for manipulating a specific repo.
3. commit- Git object that organizes a repo, connecting trees via hash codes, while being able to indicate when the repo was saved, and provides a sort bookmark indicating where the program was at the time the commit object was created.
4. repo - Short for repository, a form of directory where projects using git are periodically saved, utilizing version control and redundancy to help organize a program during its development cycle.
5. hash - Algorithmically generated string that contains huge amounts of information regarding a specific file, with practically no chance for duplication.