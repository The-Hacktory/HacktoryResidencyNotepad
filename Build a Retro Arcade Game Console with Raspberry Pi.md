# Build a Retro Arcade Game Console with Raspberry Pi

_OR: How to work in Linux on the command line so you can master any computer system and build a vintage videogame console system while we’re at it._

**_What You Need_**

*   Raspberry Pi Computer - B model or B+ (B+ model can only do HDMI video)
*   power supply (micro-usb cable, power = 1Amp)
*   4GB+ SD card (or 4gb+ micro-SD card if you are using a Raspberry Pi B+ board)
*   USB keyboard
*   thumb drive to transfer roms
*   card reader to plug into your computer to transfer the OS to your sd card
*   TV monitor w/ s-video or RCA/phono cable OR HDMI monitor w/ hdmi cable

*   _optional for fun: _usb game controller(s) (<u>[example](http://www.amazon.com/gp/product/B0034ZOAO0/ref=oh_details_o00_s00_i00?ie=UTF8&psc=1&tag=lifehackeramzn-20&ascsubtag=[type%7Clink[postId%7C498561192[asin%7CB0034ZOAO0[authorId%7C5716493564230329059)</u>)
*   _optional for sound_: ⅛” (aka 3.5mm headphone plug size) cable with dual RCA on other side to plug into the TV audio input
*   _optional for storage_: a case for your raspberry pi

**_Definitions_**

operating system

*   software that manages computer hardware and software resources and provides common services for computer programs.
*   acts as an intermediary between programs and the computer hardware,
*   can be found on almost any device that contains a computer—from cellular phones and video game consoles to supercomputers and web servers

linux

*   Linux was originally developed as a free operating system for Intel x86-based personal computers. 
*   The development of Linux is one of the most prominent examples of free and open-source software collaboration
*   It has since been ported to more computer hardware platforms than any other operating system

file system

*   used to identify a storage location in the file system.
*   File systems typically have directories (also called folders) which allow the user to group files into separate collections

shell

*   a shell is a user interface for access to an operating system's services. In general, operating system shells use either a command-line interface (CLI) or graphical user interface (GUI), depending on a computer's role and particular operation.

command line interface

*   a means of interacting with a computer program where the user (or client) issues commands to the program in the form of successive lines of text (command lines).

BASH

*   a Unix/Linux shell released in 1989
*   the default shell on Linux and Mac OS X
*   Bash is a command processor, typically run in a text window, allowing the user to type commands which cause actions. Bash can also read commands from a file, called a script.
*   it supports filename wildcarding, piping, here documents, command substitution, variables and control structures for condition-testing and iteration

emulator

*   software that duplicates (or emulates) the functions of one computer system (the guest) in another computer system (the host), different from the first one, so that the emulated behavior closely resembles the behavior of the real system (the guest)

virtual machine

*   an emulation of a particular computer system

**_Why do we emulate?_**

*   emulation is a strategy in digital preservation to combat obsolescence. Emulation focuses on recreating an original computer environment, which can be time-consuming and difficult to achieve, but valuable because of its ability to maintain a closer connection to the authenticity of the digital object
*   Potentially better graphics quality than original hardware. 
*   Potentially additional features original hardware didn't have. 
*   Save states 
*   Emulators allow users to play games for discontinued consoles. 
*   Emulators maintain the original look, feel, and behavior of the digital object, which is just as important as the digital data itself.
*   Despite the original cost of developing an emulator, it may prove to be the more cost efficient solution over time. 
*   Reduces labor hours, because rather than continuing an ongoing task of continual data migration for every digital object, once the library of past and present operating systems and application software is established in an emulator, these same technologies are used for every document using those platforms.
*   Many emulators have already been developed and released under GNU General Public License through the open source environment, allowing for wide scale collaboration.
*    Emulators allow software exclusive to one system to be used on another. For example, a PlayStation 2 exclusive video game could be played on a PC using an emulator. This is especially useful when the original system is difficult to obtain, or incompatible with modern equipment (e.g. old video game consoles which connect via analog outputs may be unable to connect to modern TVs which may only have digital inputs)

Bonus: Emulators and Art

Because of its primary use of digital formats, new media art relies heavily on emulation as a preservation strategy. Artists such as Cory Arcangel specialize in resurrecting obsolete technologies in their artwork and recognize the importance of a decentralized and deinstitutionalized process for the preservation of digital culture. -_wikipedia_

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

*   * #[ ](/ep/search/?q=%23aka&via=eqUoVqmJf3c)aka ‘wildcard’

edit text

*   nano _filename.txt_

display file

*   more _filename.txt_

_history_

# _up or down keys_

_tab_

_    _# _autocompletes a word_

**_Basic Overview of Steps To Build This Arcade Machine_**

*   Download and install your operating system (RetroPie) onto your SD card
*   Turn on your Raspberry Pi for the first time and setup EmulationStation emulator
*   Configure your controller(s)
*   Download rom files onto your personal computer, and transfer them to your pi with a thumb drive

**Step By Step Build Instructions**

STEP 1: Download and install your operating system (RetroPie) onto your SD card

What Is RetroPie?

Our operating system. A Linux OS distribution built on top of Raspbian (based on Debian, one of the most popular Linux distributions, and often used as a base for other custom operating systems). In addition to the low level processes of an operating system, there are built in emulators for consoles and other vintage computer systems, as well as a graphic interface, setup scripts, and scripts to connect game controllers. 

*   Download RetroPie Project SD card image onto your personal computer
*   Copy this “disk image” onto an SD card by typing commands in the terminal

Open up Disk Utility in the Applications > Utilities folder on your computer to see what hard drives are connected to your computer. Which Disk Number is your SD Card?

TO COPY

sudo dd bs=1m if=/Users/myHardDriveName/Downloads/RetroPieImage_ver2.3.img of=/dev/DiskNumber

SURGEON GENERAL’S WARNING: YOU MUST TYPE THE CORRECT DISK NUMBER. IF YOU CHOOSE THE WRONG ONE YOU COULD ERASE YOUR COMPUTER.

on my computer, for example

sudo dd bs=1m if=/Volumes/LaCie/RetroPieImage_ver2.3.img of=/dev/disk2

Wait 10 - 20 minutes for this to complete. _INTERMISSION: emacs games on your own computer_

*   Put the SD card in your Pi

Boot Your Raspberry Pi and Set Up EmulationStation

Plug in a keyboard, monitor, sound cable (optional), and a controller and then the power. Once it finishes booting into Emulation Station, Type F4 on your keyboard to exit to the command line. Then, follow these steps to get the SD card in order:

*   Type in sudo raspi-config to enter the configuration menu
*   Tap "Enter" on the first option to "Expand Filesystem" and wait for it run
*   Go to the Internationalisation Options and enter your location, keyboard, and timezone
*   In "Advanced Options" Select "Memory Split" and change the number to "192"
*   Select "Finish" and wait for the Pi to reboot

After it reboots, follow the onscreen prompts with your controller to set it up (up, down, left, right, etc). When you're finished, you can navigate through EmulationStation with just your controller. These controls will not work with the emulators—that takes an extra step we'll get to in the next section. After you confirm your controller works, pull up the menu (you picked the button for this during the prompts, mine is the Start button), and exit EmulationStation to go to the command line.

Step Three: Configure Your Controllers for the Emulators

With your controller and keyboard still plugged in, type this into command line:

cd RetroPie-Setup

sudo ./retropie_setup.sh

This loads the RetroPie setup screen, where we can set up our controller. Head to the third option "Setup," select "Register RetroArch Controller," and follow the on-screen directions to set up your button inputs. If your controller doesn't have the buttons it's asking for, wait a couple of seconds for the prompt to continue. When you're done back out and select "Perform Reboot." That's it, your controllers are all set up and ready to go

Step Four: Transfer Your Roms from Your Primary Computer

*   Plug in thumb drive with roms on it into the pi and plug the power back in to the pi
*   Quit emulationstation
*   Go to your roms folder, which should be:

cd /home/pi/RetroPie/roms

*   Copy off of your usb drive to your correct rom folder. To move nes files, type:

cp /media/usb/*.nes nes

cp /media/usb/*.sfc* snes/

cp /media/usb/*.bin atari2600

*   pull out thumb drive and reboot by typing:

sudo shutdown -r now

**PLAY GAMES**

**Instructions Reference**

Lifehacker blog <u>[instructions](http://lifehacker.com/how-to-turn-your-raspberry-pi-into-a-retro-game-console-498561192)</u> on setting up your RetroPie emulator system

<u>[CNET article](http://www.cnet.com/how-to/create-a-retro-game-console-with-the-raspberry-pi/)</u> on same

<u>[PetRockBlock](http://blog.petrockblock.com/)</u>: The official page for the RetroPie Project. Includes lots of guides, tips, and a forum for troubleshooting

[](http://www.raspberrypi.org/forums/index.php)<u>[http://www.raspberrypi.org/forums/index.php](http://www.raspberrypi.org/forums/index.php)</u> Lots of people are sharing their tips for getting emulators working better, as well as different controller setups, and more in the official Raspberry Pi forums.

Thread on using multiple keys to exit a game:

[](http://blog.petrockblock.com/forums/topic/use-multiple-game-pad-keys-to-exit-emulator/)http://blog.petrockblock.com/forums/topic/use-multiple-game-pad-keys-to-exit-emulator/ 

**_Emulators Reference_**

The following are built into EmulationStation

Amiga (UAE4All)

Apple II (LinApple)

Apple Macintosh (Basilisk II)

Armstrad CPC (CPC4RPi)

Arcade (PiFBA, Mame4All-RPi)

Atari 800

Atari 2600 (RetroArch)

Atari ST/STE/TT/Falcon

C64 (VICE)

CaveStory (NXEngine)

Doom (RetroArch)

Duke Nukem 3D

Final Burn Alpha (RetroArch)

Game Boy Advance (gpSP)

Game Boy Color (RetroArch)

Game Gear (Osmose)

Intellivision (RetroArch)

MAME (RetroArch)

MAME (AdvMAME)

NeoGeo (GnGeo)

NeoGeo (Genesis-GX, RetroArch)

Sega Master System (Osmose)

Sega Megadrive/Genesis (DGEN, Picodrive)

Sega Mega-CD (Picodrive)

Sega 32X (Picodrive)

Nintendo Entertainment System (RetroArch)

N64 (Mupen64Plus-RPi)

PC Engine / Turbo Grafx 16 (RetroArch)

Playstation 1 (RetroArch)

ScummVM

Super Nintendo Entertainment System (RetroArch, PiSNES, SNES-Rpi)

Sinclair ZX Spectrum (Fuse)

PC / x86 (rpix86)

Z Machine emulator (Frotz)