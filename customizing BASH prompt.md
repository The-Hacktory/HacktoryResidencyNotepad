# customizing BASH prompt

Here’s how to add an emoji icon as the command line prompt:

1.  Open Terminal app and use your preferred command line text editor to modify the .bash_profile file:

*   nano .bash_profile

1.  Go to the bottom of the doc and add a new line like the following:

*   PS1=" "

1.  Go to the Edit menu in the terminal and choose _Special Characters_
2.  Select _Emoji_ from the special character menu
3.  Find the Emoji you want to use in the shell prompt and drag & drop it into the PS1=” ” line so that it’s contained within the quotes. ![](http://cdn.osxdaily.com/wp-content/uploads/2013/04/adding-emoji-to-terminal-prompt.jpg)Depending on terminal settings, nothing may be visible after using drag & drop, but put two spaces after the blank space where the emoji was dropped, it will end up looking something like this: PS1="     "
4.  Save the .bash_profile change with Control+O (for nano) then exit out of nano with Control+X
5.  Open a new Terminal window to see the emoji as the prompt

With only an Emoji set in there, the new bash prompt will look like this:

![](http://cdn.osxdaily.com/wp-content/uploads/2013/04/emoji-bash-prompt.jpg)

You may need to enlarge your font size so that you can see the emoji. You can do this in your preferences (under the Terminal menu, choose Settings. Or Command-,)

This is more fun rather than useful per se. 

One common and particularly useful customization is to show the current working directory. That can be added by changing the PS1=” ” command to the following:

*   PS1="(drop emoji here) \W "

Or reversed:

*   PS1="\W (drop emoji here) "

And, getting increasingly useful with a username @ hostname visible with the emoji and PWD as well:

*   PS1="\u@\h (drop emoji icon) \W "

Remember to add a space (if not two) to after the Emoji or else it will be cramped against the command prompt.

If this is a bit too outrageous for you, check out **<u>[a guide to improve the overall Terminal appearance](http://osxdaily.com/2013/02/05/improve-terminal-appearance-mac-os-x/).</u>**

article from [](http://osxdaily.com/2013/04/08/add-emoji-command-line-bash-prompt/)[http://osxdaily.com/2013/04/08/add-emoji-command-line-bash-prompt/](http://osxdaily.com/2013/04/08/add-emoji-command-line-bash-prompt/)