# Intro to GitHub

**New Hacktory GitHub organization page**

[](https://github.com/orgs/The-Hacktory/dashboard)[https://github.com/orgs/The-Hacktory/dashboard](https://github.com/orgs/The-Hacktory/dashboard)

**Why Use It?**

*   track changes (a.k.a. version control = undo or go back to earlier version of your program if you made a mistake)
*   to share your code with others

**Version Control models**

*   _centralized_ - one central server. each person checks out and merges changes to a main server. only one person can "check out" the code at a time.
*   _distributed_ - each person has a local repository. when they make changes, they "check in" with the main online copy and reconcile the two together. (GitHub is this style)

**Goals of Git**

*   It's fast - add to your team and code base quickly
*   it's distributed
*   each commit has a corresponding [hash](https://en.wikipedia.org/wiki/Hash_function) (meaning every single change is tracked)
*   everyone working on the code has a local copy of the history of the program

**Notes From Lee (that weren't part of the lecture)**

*   At first, Git and GitHub are confusing! It's okay! You'll learn with practice/repetition
*   You can use GitHub on the command line/terminal or with a program (like GitHub For Mac).
*   Yes, this is _the _standard that most people use to distribute code
*   You can even use this to post just text or other non-code files online
*   People like using GitHub because it allows them to easily share code, write notes about it, find code from other people, and even allow people to easily comment and offer code suggestions to each other
*   We primarily started using GitHub in the terminal, which is why the notes you see below are all terminal commands. We switched to the GitHub application near the end.
*   A mental model to use: Pretend you are working on a Word document and you hit undo. Then you hit undo again. Then again. GitHub is a much more robust way to go back and forth in different versions of your own code. (that's called version control). 
*   _You add and commit your code on your own computer (git), and when you are ready you push it online to your repository on your github page._
*   If you fork (aka copy) someone else's code/program, you pull it onto your computer so that you can edit the code. Afterwards, you can push it to your own online repository (aka repo) or you can do a pull request to the original code and that person will look at your code and decide to integrate the two together (or not).

**Installation**

[](http://git-scm.com/downloads)http://git-scm.com/downloads

*   git config --global user.name "Your name Here"
*   #sets the default name for git to use when you commit
**   git config --global user.email "your_email@example.com"
*   #sets default email for git 
**   git config --list
*

**Your first tracked file**

*   use a text editor and save a text file called hello_world.txt to your folder
*   tell git to track changes

*   git add hello_world.txt
*   git status

*   File is now tracked by git
*   Tell git to commit the file

*   git commit -m "First commit. Added hello world to repository."
*

**What did we just do? (How is this different than saving a file?)**

1.  When we add a new file, we tell Git to add the file to the repository to be tracked
2.  when we stage an exiting file, we are telling Git to track the current state of the file
3.  A commit saves changes made to a file, not the file as a whole. The commit will have a 'hash' so we can track which changes were committed when and by whom

**To see all your commits**

*   git log

OR

*   git log --pretty=oneline
*

**GUI/Graphical Interface**

[](http://git-scm.com/downloads/guis)http://git-scm.com/downloads/guis

**Undoing Local Changes If You Make A Mistake**

*   git rm -f my_incorrect_file.txt
*

**Branching**

*   git checkout -b version2

Adding new lines

*   git add hello_world.txt
*   git commit -m "Adding changes"

Find which branch you're in

*   git branch

**Merging Branches**

*   git merge version2

**Merging the master into version2**

*

**Get local repository of github on machine**

*   cd ..../ #back to root directory
*   mkdir hello-github
*   cd hello-github
*   git init
*   git remote add origin [](https://www.github.com/yourURLFromYourRepository)https://www.github.com/yourURLFromYourRepository
*   git pull origin master
*

**Push to Github Repo**

Edit the ReadMe file

*   git add README
*   git commit -m "Updating readme file"
*   git push origin master

 