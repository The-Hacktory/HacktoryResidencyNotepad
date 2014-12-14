# Programming and Project Glossary and Languages

_This hackpad contains a glossary and then a list of programming languages and frameworks and describes them in plain english and links to a tutorial for each._

**GLOSSARY**

**IDE** (integrated development environment) is a software application that provides comprehensive facilities to programmers for software development. An IDE normally consists of a source code editor, build automation tools and a debugger. Processing and Arduino have their own IDE application but you can write code in other IDEs such as XCode as well. Examples: XCode (for C++, OpenFrameworks, Objective C, etc), IDLE (for Python), Arduino (for Arduino), Processing (for Processing)

**Programming Language - **A programming language is a formal constructed language designed to communicate instructions to a machine/computer. Examples: Java, Javascript, Python, C, C++

**Framework - **A software framework is a universal, reusable software platform to make it easier to build programs. A framework can contain elements such as: a programming language, an Integrated Development Environment (though OpenFrameworks does not which is why you use it inside XCode), support programs, compilers, code libraries, tool sets, and application programming interfaces (APIs) that bring together all the different components to enable development of a project. Examples: Processing, OpenFrameworks

**API **(application program interface) - Specifies how some software components should interact with each other. The practice of publishing APIs has allowed web communities to create an open architecture for sharing content and data between communities and applications. In this way, content that is created in one place can be dynamically posted and updated in multiple locations on the web. Examples include photos can be shared from sites like Flickr and Photobucket to social network sites like Facebook and MySpace. Content can be embedded, e.g. embedding a presentation from SlideShare on a LinkedIn profile.

_format_

**Programming LANGUAGE or Framework or IDE**

*   Plain english description
*   Link to a tutorial

**[Arduino](http://www.arduino.cc/en/)** 

**   Arduino is the name for the hardware device as well as the name of the programming language that you write to control it and the IDE environment as well. The arduino language is based on C, influenced by Processing and Fritzing. Why learn it? Build your own devices, interactive installations, hardware, machines, etc. from simple to extremely complicated. You can start as a beginner and use pre-written code and as you learn more and more you can build things from scratch or customize code entirely. There is a huge community of tens of thousands (millions?) of artists worldwide that use arduino. FREE for the software. The arduino hardware costs money, generally $10-75 depending on how extensive an arduino you need.
*

**[Processing](http://www.processing.org)**

**   is an open source programming language and integrated development environment (IDE) built for the electronic arts and visual design communities. It builds on the graphical side of Java, simplifying some features and adding new ones. It is developed by Casey Reas and Ben Fry. It is designed to make it easy to use for new programmers as well as for those familiar with other languages. It is particularly suited for creating "generative" visual art, working with visuals based on data, and for making interactive software and installations. It can work with arduino as well, replacing the arduino language on an arduino board. [](http://www.processing.org)http://www.processing.org FREE

*   tutorials:
*   I like [this book ](https://learningprocessing.com)and website by Daniel Shiffman.
*   We also have [this shorter book](http://www.amazon.com/Getting-Started-Processing-Casey-Reas/dp/144937980X/) by Processing's inventors in our Hacktory library.

**[Processing.js ](http://en.wikipedia.org/wiki/Processing.js)**

**   is a JavaScript port of Processing (in other words, you write your program in Processing and the machine turns it into Javascript language instead of Java, a different though similarly-named language). This is still intended as a programming language designed to write visualizations, images, and interactive content. It's used specifically to create programs that launch in a web browser to display animations, create visual applications, games and other graphical rich content without the need for a Java applet or Flash plugin. FREE
**   If you know regular Processing, then you know most of Processing.js 
*   A tutorial on the differences and how to use processing.js is [here](http://processingjs.org/articles/p5QuickStart.html).
*

**[iProcessing](http://luckybite.com/iprocessing/)**

**   iProcessing is an open programming framework to help people develop native iPhone applications using the Processing language. It is an integration of the Processing.js library and a Javascript application framework for iPhone. The iProcessing [download](http://iprocessing.googlecode.com/files/iProcessing-0008.tar.gz) consists of a set of example XCode projects that demonstrate many of the Basic Examples from the [Processing](http://processing.org/learning/basics) web site (originally written by Casey Reas and Ben Fry unless otherwise stated) as well a number that demonstrate the use of various iPhone features such as multitouch, accelerometer, orientation, location, sound play/record, app state saving and so on. Processing was created by Tom Hulbert at [Luckybite](http://luckybite.com/) in 2009.
*   FREE

**XCODE**

*   Xcode is an integrated development environment (IDE) containing a suite of software development tools developed by Apple for developing software for OS X and iOS. It is free on Mac computers. You would use XCODE to write your programs in C++, Objective C, OpenFrameworks, and other languages.

*   Good tutorial/introduction [here](http://codewithchris.com/xcode-tutorial/).
*

**[J](http://en.wikipedia.org/wiki/JavaScript)[avascript](http://en.wikipedia.org/wiki/JavaScript)**

**   **JavaScript** (**JS**) is a juggernaut computer programming language, probably the most important and by far the most widely used language today. Almost all dynamic web apps are built in Javascript.  In the past few years it has even been used to write programs that work outside on the browser, when used with a framework called  [Node.js](http://en.wikipedia.org/wiki/Node.js) to create games and other desktop and mobile applications. Despite the name Javascript and Java are not related.

Hundreds of free tutorials online.

I've tried the [Codecademy](https://codecademy.com) one (slightly more beginner friendly)

and [this one](http://eloquentjavascript.net/) (shorter course, with slightly more conceptual ideas than just pure coding tutorial)

*

**[J](http://en.wikipedia.org/wiki/Java_(programming_language))[ava](http://en.wikipedia.org/wiki/Java_(programming_language))**

**   **Java** is a language intended to let application developers "write once, run anywhere" meaning that code that runs on one platform does not need to be recompiled to run on another. Java is one of the most popular languages in the world. Java was originally developed by James Gosling at Sun Microsystems (which has since merged into Oracle Corporation) and released in 1995 as a core component of Sun Microsystems' Java platform. The language derives much of its syntax from C and C++, but it has fewer low-level facilities than either of them. In other words, C and C++ are usually said to run their programs much faster, but Java is designed to be easier and simpler to write. Despite the name Javascript and Java are not related.
*

**[C](http://en.wikipedia.org/wiki/C%2B%2B)[++](http://en.wikipedia.org/wiki/C%2B%2B)**

**   **C++** (pronounced _cee plus plus_) is a general purpose programming language. It is built and influenced by C, specifically intended as an object-oriented language. An object oriented language is the idea that the programmer creates or copies "objects" that have data fields (attributes that describe the object) and associated procedures known as methods. Objects, which are usually instances of classes, are used to interact with one another to design applications and computer programs.
*   C++ is not beginner friendly. OpenFrameworks is a framework built on top of C++ designed to make it easier for artists to build programs.

**[C](http://en.wikipedia.org/wiki/C_(programming_language))**

**   In computing, C is a general-purpose programming languageinitially developed by Dennis Ritchie between 1969 and 1973 at AT&T Bell Labs. C is one of the most widely used programming languages of all time, and C compilers are available for the majority of available computer architectures and operating systems. Many later languages have borrowed directly or indirectly from C. Why would you use C? To built blazing fast programs.

**[openFrameworks](http://en.wikipedia.org/wiki/OpenFrameworks)**

**   **openFrameworks** is an open source toolkit designed for "[creative coding](http://en.wikipedia.org/wiki/Creative_coding)". OpenFrameworks is written in C++ and runs on Windows, Mac OS X, Linux, iOS, and Android. It is maintained by Zachary Lieberman, Theo Watson and Arturo Castro with contributions by other members of the openFrameworks community.

Introduction with tutorials and examples [here](http://www.openframeworks.cc/tutorials/introduction/000_introduction.html).

**[P](http://en.wikipedia.org/wiki/Python_(programming_language))[ython](http://en.wikipedia.org/wiki/Python_(programming_language))**

**   Python is a widely used general-purpose, high-level programming language. Its design philosophy emphasizes code readability, and its syntax allows programmers to express concepts in fewer lines of code than would be possible in languages such as C. The language provides constructs intended to enable clear programs on both a small and large scale, for beginner and advanced coders.
**   Python supports multiple programming paradigms, including object-oriented,imperative and functional programming or procedural styles. Like other dynamic languages, Python is often used as a scripting language, but is also used in a wide range of non-scripting contexts. Using third-party tools, such asPy2exe or Pyinstaller, Python code can be packaged into standalone executable programs. Python interpreters are available for many operating systems. On Mac, the Python IDE is called IDLE.

tutorials: There are many online but I don't know of one aimed specifically at the artistic community (Develop it and you can probably make some money!). The most beginner friendly tutorials are probably at [codecademy](http://www.codecademy.com/en/tracks/python) and the [Invent With Python](https://inventwithpython.com) book/site.

**[Wiring ](http://wiring.org.co/)**

**   is a programming environment and electronics i/o board for exploring the electronic arts, tangible media, teach- ing and learning computer programming and prototyping with electronics. It is an open project initiated by Hernando Barraga`n and builds on Processing. [](http://wiring.org.co/)[http://wiring.org.co/](http://wiring.org.co/)
**

**Fritzing**

*   A program designed to help with the layout of circuits - kind of like scratch where each item is an icon/image.  Allows for easy prototyping/sharing of circuit maps.

**[Max/MSP](http://www.cycling74.com/)**

**   is a graphical development environment for music and multimedia. The program is highly modular and allows the development of third-party externals as objects which can be fully integrated with the native libraries. A typical Max program, called a ‘patch’ is based on multiple graphical objects connected into a data flow and looks like the way you snap bricks together inside Scratch. Max was originally developed by Miller Puckette and is now developed and maintained by Cycling’74.  It costs $300 but 1-year student licenses are $100 I think.
**   www.cycling74.com

**[Jitter](http://www.cycling74.com/)**

**   Built into Max. It extends the Max/MSP programming environment to support realtime manipulation of video, 3D graphics and other data sets within a unified processing architecture.
**   www.cycling74.com

Tutorial: Read the Max Tutorials available inside Max first, then try [these](http://cycling74.com/2006/02/06/jitter-recipes-book-1/) to learn how to build your own visual generator recipes.

**[ChucK](http://chuck.cs.princeton.edu/)**

**    is a concurrent, strongly-timed audio programming language for real-time synthesis, composition, and performance, which runs on Mac OS X, Linux, and Windows. Code can be added, removed and modified on the fly, while the program is running making it an ideal language for live coding. It was originated by Perry Cook and Ge Wang of Princeton University. 
**   [](http://chuck.cs.princeton.edu/)[http://chuck.cs.princeton.edu/](http://chuck.cs.princeton.edu/)
*

**[Csound ](http://www.csounds.com/)**

**   is a text based music programming language written in the C programming language. A typical Csound program will include an _orchestra _file describing the nature of the instru- ments and a _score _file describing the parameters of the ma- terial (pitch, duration, amplitude etc). Csound then ren- ders these files to produce an audio file or real-time audio stream.
**           [](http://www.csounds.com/)[http://www.csounds.com/](http://www.csounds.com/)

**[Pure Data](http://puredata.info/)**

**   is a graphical programming language developed by Miller Puckette (inventor of MaxMSP) in the 1990s for the creation of interactive computer music and multimedia works. Though Puckette is the primary author of the software, Pd is an open source project and has a large developer base working on new extensions to the program. It is released under a license similar to the BSD license. It is essence an opensource and free alternative to Max/MSP.
**   [](http://puredata.info/)[http://puredata.info/](http://puredata.info/)
*

**[OSC](http://www.cnmat.berkeley.edu/%20OpenSoundControl/)**

**   is a protocol for communication among computers, sound synthesisers and other multi-media devices. It is optimised for networking technology allowing very fast data sharing between machines. It can transport over many protocols but is commonly used with UDP or TCP/IP. It can be com- pared to MIDI, but does not suffer the same time lags and allows an open-ended url-style symbolic naming scheme. [](http://www.cnmat.berkeley.edu/)[http://www.cnmat.berkeley.edu/](http://www.cnmat.berkeley.edu/) OpenSoundControl/
*

**[SuperCollider ](http://www.audiosynth.com/)**

**   is a real time audio synthesis programming language. The Language combines the object oriented structure of Smalltalk and features from functional programming lan- guages with a C programming language family syntax. Originating as proprietary software, it was released in 2002 by its author James McCartney under the free sofware GPL license.
**   [](http://www.audiosynth.com/)[http://www.audiosynth.com/](http://www.audiosynth.com/)
***    