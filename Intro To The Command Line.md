# Intro To The Command Line

**What is the command line?**

The **command-line interface**, sometimes referred to as the CLI, is a tool into which you can type text commands to perform specific tasks—in contrast to the mouse's pointing and clicking on menus and buttons. Since you can directly control the computer by typing, many tasks can be performed more quickly, and some tasks can be automated with special commands that loop through and perform the same action on many files—saving you, potentially, loads of time in the process.

The application or user interface that accepts your typed responses and displays the data on the screen is called a **shell**, and there are many different varieties that you can choose from, but the most common these days is the **Bash** shell, which is the default on Linux and Mac systems in the **Terminal** application.

**Philosophy**

*   The OSX command prompt is a place where you can type commands to manipulate files on your computer or launch programs that perform complex tasks.
*   In some ways the command prompt is the _simplest_ kind of computer interface. You are probably more familiar with interfaces that have windows and buttons, but the command prompt is an interface entirely driven by text input. Type a command. The command is performed. You are prompted to enter another command. Yes, it is _that_ simple.
*   Writing a program for the command prompt is _much easier_ than writing a program with a graphical interface (windows and buttons). So much easier, in fact, that the majority of programs written today are written for the command prompt. This is why learning to use the command prompt will open up a whole new world for you. You will have access to a vast array of programs and technologies that were previously off-limits. 

*   _taken from _[The Designers Guide To The OS X Command Prompt](http://wiseheartdesign.com/articles/2010/11/12/the-designers-guide-to-the-osx-command-prompt/)

**Why would I use this or need to know this?**

*   simplicity and minimalism (see [article](http://en.wikipedia.org/wiki/Unix_philosophy) on Unix philosophy)
*   ubiquity - nearly every computer from OS X, Raspberry Pi to web servers, internet devices, routers and robots can be controlled through the command line, and even more devices are being created that can be interacted with that are online (the so-called "Internet Of Things")
*   Works on devices that don't have a screen, mouse, etc
*   Some tasks are lightyears faster (instant) when calling the command from the command line instead of using a specific application or having to find a specific program to download from the internet
*   write your own scripts for common commands/procedures that you need to do on your computer (_random example: you could create a command to batch resize a folder of photos and rename them.)_

**Working With The Command Line on OS X**

*   On a Mac, you use the "Terminal"
*   Inside the Applications Folder is a folder called Utilities. Inside the Utilities is the application Terminal. Doubleclick it to open.
*   Now that you've got this open, it's time to try out simple commands or do a tutorial

**Okay, but how do people actually use this thing? Why should I care?**

*   The terminal is ideal when you want to do things super quickly without taking minutes or sometimes hours to do the same thing inside a traditional program on your computer. Instead of opening a program, clicking around, trying to find what you need, or maybe it not having what you need, you can type a few words and in seconds be finished. 
*   Examples: instead of going in individually and opening and closing menus and choose export and resize options for each photo in photoshop, imagine you type just 5 words in the terminal and all your photos in a single folder are resized instantly
*   Many people use the terminal to jump between folders and move files quickly on their computer
*   It's also ideal for taking the output of one program and then sending it as input to another program (known as _piping_)
*   Do you need to do something on your computer but there is no specific program out there that does it exactly? Write it in the terminal. 

*

**Tutorials**

[A Command Line Primer For Beginners](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything/all) - _article for beginners on Lifehacker_

[An Introduction To The Command Line](http://en.flossmanuals.net/command-line/index/) - _a more extensive online open-source manual_

[The Command Line Crash Course](http://cli.learncodethehardway.org/book/) 

[Learning The Bash Shell](http://shop.oreilly.com/product/9780596009656.do) - _a book we have in The Hacktory's library_

[An A-Z Index Of All Commands Possible On The OS X Command Line](http://ss64.com/osx/)

**_Some basic BASH commands_**

Print Working Directory

*   pwd

List Files

*   ls
*   ls -1

Change Directories

*   cd _directory_
*   cd ..

Copy a file

*   cp _filename_

Remove a file (Not trash)

*   rm _filename_

*   * #[ ](https://thehacktoryresidency.hackpad.com/ep/search/?q=%23aka&via=eqUoVqmJf3c)aka ‘wildcard’

edit text

*   nano _filename.txt_

display file

*   more _filename.txt_

_history_

# _up or down keys_

_tab_

_    _# _autocompletes a word_