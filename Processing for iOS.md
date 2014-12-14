# Processing for iOS

Info gleaned from the online Creative Coding course here:

[](https://class.coursera.org/digitalmedia-002)https://class.coursera.org/digitalmedia-002

**Setting up Javascript in Processing**

1.  Go to the top right of your processing window (in the IDE) and click where it says Java and select "add mode" and choose Javascript.
2.  You're done!

**Prototyping / Running Your Processing Sketch live on your iOS Device**

1.  IMPORTANT: Both your iOS device and your computer need to be running on the same wifi network for this to work!
2.  Open your terminal application (on a mac, it's in your applications folder within the Utilities folder.) Type the word "ifconfig" and it'll spit out a lot of gobbledygook. Find the IP address to the right of the word "inet." For example mine is 192.168.4.5
3.  Go back into processing and "hit play" which really actually tells your computer to start a server running on your machine!
4.  When you run it, your web browser will automatically launch (I'm using Chrome). In the address bar, note the number after the colon. That's called a port or port number. It's like a channel. So, for example, my address bar says 127.0.0.1:64474. So the number 64474 is the port. By the way, you can try out your sketch in your web browser on your computer if you want.
5.  Go to your iOS device and open your browser (I'm using the standard safari browser built in to the iphone). Go to the address bar and type http:// and then type the number you found to the right of the inet (for me that is 192.168.4.5) and then type in the port number (for me that was 64474). So for me I type in [](http://192.168.4.5:64474)http://192.168.4.5:64474 This address is local to my machine and won't work on yours!
6.  It should now launch in the browser on the iphone/ipad!

**Templates for creating sketches for Android/iOS/Desktop Apps**

Download [here](https://class.coursera.org/digitalmedia-002/wiki/Code).