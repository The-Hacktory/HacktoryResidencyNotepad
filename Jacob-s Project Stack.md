# Jacob's Project Stack

**To Do**

*   Sign up for classes
*   Create Project Stack

*   Do more sketching/prototype drawing

**Things I Want To Learn/Do**

*   Learn how to integrate real-time data (tidal charts, weather, GIS data, sensors, etc) into Processing so it can be visualized as both data and physical motion within a sculpture (activation motors/lights) - _after learning basics of Processing, look into learning Arduino and/or Firmata, which lets you control an arduino board with Processing instead of the Arduino language - Lee 6.18_

Lee - last night you mentioned that Python would be a better language to gather GIS/GPS data.  If I wanted to use this data to then turn a motor in a particular direction - which language would it be best to focus on? 

*   _hey jacob, there are ways to do this to combine python w/ arduino. several of the books we acquired in our library have examples of how to do this. openFrameworks and even Processing can probably do this as well. let's look at the book examples and discuss ways to do this together with 1 or 2 of our expert advisors. i'm now thinking it's time to arrange meeting between you guys and our advisors in early july so everyone can start moving forward on this kind of stuff and get into the nitty gritty details of their projects while improving their coding skills and coming up with project plans. the truth is that you can do almost anything in any language, but each language has its own things it's better at. python is great for working with large amounts of data from the internet. processing is great at making things simple, and making beautiful easy-to-manipulate visualizations. openFrameworks (generally referred to as "oF") is good at working super duper fast and for being able to integrate with tons of other programming languages and on many different kinds of systems and being super modular/customizable. all 3 have communities of artists working in them.-lee 6.19_

Lee - Can we get this book - [Open-Source Lab: How to Build Your Own Hardware and Reduce Research Costs](http://www.amazon.com/Open-Source-Lab-Hardware-Reduce-Research/dp/0124104622/ref=sr_1_1?ie=UTF8&qid=1403291089&sr=8-1&keywords=Open-Source+Lab%3A+How+to+Build+Your+Own+Hardware+and+Reduce+Research+Costs)

*   _-Hey Jacob, short answer: yes, but can it wait one week until Georgia returns from her vacation so I can order it?_
*   Totally cool.
*   Hi there, Jacob I think I can order that book for you. Also, we've been doing some stuff with sensors and gathering data for DMD. One of the guys working on it set up a mini web server using Ruby in the course of a few hours. I think it might be good if you came the next time we worked on that stuff, which should be in the next week or so. I'll copy you on my message to that group if you don't mind.

Please do!

*   Learn how to program small lcd or OLED displays.
*   How to read schematics
*   How to wire circuits correctly (no more melted wires or breadboards!) You should totally come to our Intro to circuits class next week! The content may already be familiar to you, but it would be a great time to start talking with Doug Poole, who is an Electrical Engineer, a great teacher, and is interested in getting involved as a mentor.

Signed up for it!

*

**Things I'm interested in right now**

*   South Pointing Chariot - not the machine itself, but the ideas behind its creation and relative use - [](http://en.wikipedia.org/wiki/South-pointing_chariot)http://en.wikipedia.org/wiki/South-pointing_chariot
*   Everything in this book - most particularly essays on Sentimentality/Place: [](http://www.amazon.com/Madness-Rack-Honey-Collected-Lectures/dp/1933517573)http://www.amazon.com/Madness-Rack-Honey-Collected-Lectures/dp/1933517573
*   Synthetic Aesthetics and Alexandra Daisy Ginsberg: [](http://www.syntheticaesthetics.org/)http://www.syntheticaesthetics.org/
*   [Maps of the Imagination: The Writer as Cartographer ](https://- https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&uact=8&ved=0CB8QFjAA&url=http%3A%2F%2Fwww.amazon.com%2FMaps-Imagination-The-Writer-Cartographer%2Fdp%2F1595340416&ei=ohWjU7XSJfPMsQSXjILIDg&usg=AFQjCNGJQSSHOgGcbexsKqC_yLVlv8IR4g&sig2=8Gn-m_9iEoE6i1k-yB9a8g&bvm=bv.69411363,d.cWc)
*   Real-time data - placing sensors in the water or wind that transmit signals via bluetooth or wifi

**Processing HOMEWORK**

I set up the circle to increase in size and change in color as it read the seconds on the computer.  With each mouse click it would show the corresponding seconds, shifting over as time increased.

  I couldn't quite figure out how to switch between the two (image and text) - so that clicking would clear the screen and just show seconds, or just show the visualization of time passing.

*     _-hey jacob : question? i tried running your could and it hit me back with a **"cannot convert from void to int" _**_Is there a library i should import? or a piece of code im missing?_
*   -_this happened to me too. _

hmm, I just retried it in here - [](http://semmy.me/ide/)http://semmy.me/ide/ and it worked, so not totally sure.  - maybe double checking that the last two "}" are there.

*   -_hmmmmmm. runs fine on the processing.js site. What is the processing.js website in the first place? is it an online environment to run and compile processing? im suspecting that it has libraries of it very own and maybe that would explain why it wouldnt run on my  Laptop based Processing environment... **<u>LEE??????????????????</u>_**

*   _-Processing.js is a JavaScript port of Processing. There are some significant differences and you should read about them [here](http://www.aosabook.org/en/pjs.html)._

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1403113358341_Screen shot 2014-06-18 at 1.40.20 PM.png)

**CODE**

int value = 0;

*   int value1 = 0;
*   int value2 = 0;
*   int s = second();  
*   int m = minute();
*   int h = hour();
**   void setup() {
*     size(600,600);
*     background(255);
*   }
**   void draw() {
*     noStroke();
*     fill(value, value1, value2);
*     ellipse(100,hour()*10, 100, 100);
*     ellipse(200, minute()*10, 100, 100);
*     ellipse(300, second()*10, 100+ second()*10, 100);
*     }
*      void mousePressed(){
*     textSize(50);
*     text(second(),50+ (second()*5),410);
*     }
*     void minute(){
*     if (value == 0) {
*       value = random (0,255);
*     } else {
*       value = random (0,255);
*     }
*     if (value1 == 0) {
*       value1 = random (0,255);
*     } else {
*       value1 = random (0,255);
*     }
*     if (value2 == 0) {
*       value2 = random (0,255);
*     } else {
*       value2 = random (0,255);
*     }
*     }
*

**Questions To Ponder**

*   Was this easy/hard?

Easy

*   What was the point of the Angry Birds code tutorial?

Getting us to understand that what we want to have happen in a program is broken down into simple steps.  Also the direct relationship between code/language/what-goes-on-behind-the-bird/input and output/visualization.

*   Were you surprised by how quickly you made something in Processing?

Yes (but I've also done a little of this before)! 

*   What do you like about coding in Processing? What do you find difficult?

I love that it can transform images, break them down and build them up again.  

The math is difficult ... and - for() loops always get me when writing them

*    

**ARTISTS: art + tech**
<ul style="list-style: none;"><li>Artists:</li>
<li>_Nils V**[Ö](http://en.wikipedia.org/wiki/%C3%96)_**_elker_</li>
<li>The ephemeral gestures of the inflation/deflation is what draws me in.</li>
<li>[](http://www.nilsvoelker.com/content/onehundredandeight/)http://www.nilsvoelker.com/content/onehundredandeight/</li>
<li>![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1403718978564_Screen shot 2014-06-25 at 1.56.01 PM.png)</li>
<li>_Tim Hawkinson_</li>
<li>Incredibly influential - one of my first introductions to art and tech - his playfulness/seriousness/analog/exposed systems is incredible.   

*   -OMG Samesees!!!! Tim Hawkinson book would be a wonderful surprise gift to any artist, most importantly ME!!!!! awesome list homie - max_ _
*   Thanks! - his exhibit at Whitney in 2007 was one of the best art exhibitions I've ever been to.
*</ul style="list-style: none;">

*   [](http://www.pacegallery.com/artists/175/tim-hawkinson)http://www.pacegallery.com/artists/175/tim-hawkinson
*   ![](http://concepttwo.files.wordpress.com/2011/09/spin-sink.jpg)

[](http://concepttwo.files.wordpress.com/2011/09/spin-sink.jpg)http://concepttwo.files.wordpress.com/2011/09/spin-sink.jpg

**   _John Cage's Chess Board (v. Duchamp)_
*   I love love love this piece.  Contact microphones embedded in the board create the symphony for the game. 
*   ![](http://laughtersounds.files.wordpress.com/2012/10/duchamp_cage_playing_chess.jpg)

[](http://laughtersounds.files.wordpress.com/2012/10/duchamp_cage_playing_chess.jpg)http://laughtersounds.files.wordpress.com/2012/10/duchamp_cage_playing_chess.jpg

**   _Dane Winkler_
*   Though not exactly art/tech - the combination of wood/tech aesthetic is hard to resist.
*   [](http://www.danewinkler.net/the-hobo-film-fest)[http://www.danewinkler.net/the-hobo-film-fest](http://www.danewinkler.net/the-hobo-film-fest)

*   ![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1403718947846_Screen shot 2014-06-25 at 1.55.24 PM.png)

*   _WIND MAP - Hint.fm_
*   One of the main things I want to get out of this residency is to learn how to call in outside data sets to create real-time data visualizations ... like this
*

[](http://hint.fm/wind/)http://hint.fm/wind/

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1403719731424_Screen shot 2014-06-25 at 2.08.19 PM.png)

*   _Daisy Ginsberg_
*   More conceptual - but reliant on current ideas around bio-tech and art
*   [](http://www.daisyginsberg.com/work/echromi-limited-editions)[http://www.daisyginsberg.com/work/echromi-limited-editions](http://www.daisyginsberg.com/work/echromi-limited-editions)

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1403719016719_Screen shot 2014-06-25 at 1.56.40 PM.png)

Krzysztof Wodiczko

Alien Staff

[](http://web.media.mit.edu/~jrs/krz/alien.html)http://web.media.mit.edu/~jrs/krz/alien.html

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1403719154317_Screen shot 2014-06-25 at 1.59.02 PM.png)

**Project for July**

What I would like to do is to update a version of this project on a smaller scale: 

[](http://www.jacobrivkin.com/work/catenary-for-aeolus/)http://www.jacobrivkin.com/work/catenary-for-aeolus/

I used an Arduino to turn off and on a vacuum motor and fan motor, which were connected via a large light-plastic form, to look like they were breathing.  The pattern was based on video I shot in Newfoundland and the ebb and flow of the tide coming in.  I timed when each one went in and out and created a case system in the .ide to run the program (I can post that code later).  What I really want to learn is how to actually synchronize this "ebb and flow"  with real-time data from the interwebs.  

So - this means I need to:

*   Learn API!!!!
*   Get a new Arduino (Lee do we have any we can use?) 
*   Get a WiFi Shield for Arduino
*   Get another vacuum and fan motor
*   Get a relay shield (Do we have any at the Hacktory?)

*   _if your broke i can show you how to make an up to 8+ output relay setup using standard relays from radio shack, some resistors, blowback diodes, and a couple of registers. (i use the same set up to control all my animatronics) If the aurdino board you are using has enough digital and/ or analog outputs for the number of motors you are trying to control then we dont need the shift register / demux (DE-MULTIPLEXER ) , but im sure at some point you will want to control more then the outputs provided so if your down,  i would be interested in learning what code is needed to send what i would imagine would be clock data on one output and serial data on the other to a demux chip (takes the one stream and turns it into many streams) to control all those motors. - max_
*   I would love to learn how to make them in-house regardless of cost.  What was interesting about the code I was using for the fan and the motor was that I brought them in as analog inputs - which meant I could control their respective speeds using 0-255.  The vacuum was crazy fast regardless so I kept it at 1.  But it was interesting to be able to control the speeds with the Arduino.
*   _PS what kind of motors are you trying to control? Let me know the AMP rating so i can help you figure out the type of relays. Also, have you played with SERVOS (unlike standard motors, servo motion can be controlled by very tiny increments as well as change direction) eat all? I know that arduino is really great at sending and controlling seRvoS (camel humping!)_
*   Stepper motors - I think I would go for ones that use the lowest amount of energy/amp possible.  The weight load won't  be very much since it will be positioned vertically.

 ![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1403800214577_Screen shot 2014-06-26 at 12.29.55 PM.png)

I've used servo motors before.  I built a shovel that closed up on itself when it got dark out (lightsensor -> servo control).  It kind of worked.  The servo motor wasn't exactly strong enough to lift the shovel head - and it kind of bounced around then I think broke a few of the teeth in the servo ... I have pics of it somewhere - I'll find em soon and post it.   

If this isn't doable on a month scale (I think it totally is) - the other option is to build a sensor that can monitor real-time data.  I could build a sensor to put by the piers by Bartram's Garden to measure tide or wind speed, and have that data then do "X".  Another part of this could be to learn how to use that data it collects to then be broadcast via WiFi ([](http://www.flutterwireless.com/))http://www.flutterwireless.com/) which then shows a visualization on a screen nearby.

*   Get a new Arduino
*   Get a wifi shield
*   Build a sensor
*   Learn how to broadcast the data collected (I'm guessing  the data is sent to the serial port, and that is what is broadcast?)
*   Design visualization to represent what happens when data is collected
*   Figure out solar input - I've been looking at these: [](http://www.rei.com/product/836250/goal-zero-boulder-15-solar-panel#reviewsTab)http://www.rei.com/product/836250/goal-zero-boulder-15-solar-panel#reviewsTab to contemplate if there is a way to make the sensor self-sustaining.

Also - Learn how to access this biz.

 [](http://tidesandcurrents.noaa.gov/waterlevels.html?id=8545240)http://tidesandcurrents.noaa.gov/waterlevels.html?id=8545240

[](http://co-ops.nos.noaa.gov/api/)http://[co-ops.nos.noaa.gov/api/](http://tidesandcurrents.noaa.gov/waterlevels.html?id=8545240)

**Jacob, Michael, Max - check this out:**

[10 Pieces Of Music Created By Brainwave](http://thecreatorsproject.vice.com/en_au/blog/10-pieces-of-music-created-by-brainwaves?utm_source=tcptwitteranz)

Electromagnetic Waves + Sound in Forests/Ocean/Landscapes

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1404915579745_undefined)

[](http://www.vlf.it/romero2/explorer-e202.html)http://www.vlf.it/romero2/explorer-e202.html

TREE ANTENNAS?!

_super useful - ml_

What about making circuits that "grow" and "change" based on biological and chemical environmental reactions??? Like electro-conductive molds? Do those exist? i guess thats how shit works any ways but it would be fun to make a moldy bread circuit that was powered by decomposing lemons and powers the butt end of fireflies ....

WIND CODE

This code works to get the windspeed data from the Wunderground API onto the Arduino using the WifiShield (Arduino brand) and prints it to the Serial Monitor - <s>the one thing I'm having trouble with is getting the wind_mph to be an integer.  I've tried using toInt() and atoi() ...but to no avail...</s>

Got it working!!  With Tim's help - I was able to convert the string to a string of characters, and then replace the ">" with a "".  Now it's an integer I can use as an input to map the speed to the fan motor.

<s>I was having one slight issue with the WUnderground API blocking my request, but I changed the server from: </s>

<s>char server[] = "api.wunderground.com";   </s>

<s>to:</s>

<s>IPAddress server (38,102,136,138);</s>

<s>I'm still having some server issues - not sure what's up with it.  I emailed with the folks at the wunderground and they said it's not on their end. so I dont know.</s>

IT WORKS IT WORKS!!!!!!!!!

*    
***   /*
*     Web client
*    
*    This sketch connects to a website ([](http://www.google.com))http://www.google.com)
*    using a WiFi shield.
*    
*    This example is written for a network using WPA encryption. For 
*    WEP or WPA, change the Wifi.begin() call accordingly.
*    
*    This example is written for a network using WPA encryption. For 
*    WEP or WPA, change the Wifi.begin() call accordingly.
*    
*    Circuit:
*    * WiFi shield attached
*    
*    
*    created 13 July 2010
*    by dlf (Metodo2 srl)
*    modified 31 May 2012
*    by Tom Igoe
*    */
*   int windN = 0;
*   #include <SPI.h>
*   #include <WiFi.h>
*   //#include <stdlib.h>
**   char ssid[] = "Dept of Making + Doing";
*   char pass[] = "RobotZebra";
*   //char ssid[] = "28107be15097";
*   //char ssid[] = "Dr. Sandor Katz";           //  your network SSID (name) 
*   //char pass[] = "BULY2U633TL9C46I";  // your network password (use for WPA, or use as key for WEP)
*   //int keyIndex = 0;            // your network key Index number (needed only for WEP)
*   String apiState = "PA";                 //  the state where you want to montitor weather (in a two letter format)
*   String apiCity = "Philadelphia";         //  the state where you want to monitor weather (each word should be capitalized, replace space with an underscore i.e. New_York).
*   String apiKey  = "daf825a0fc92c02b";
*   String GETRequest = "GET /api/" + apiKey + "/conditions/q/"+ apiState + "/" + apiCity +".xml HTTP/1.1";
*   String currentLine = "";
*   String wind = "";
*   boolean readingWind = false; 
*   //int windMotor;
*   //char windSpeed[1];
*   int motorPin = 9;
**   const unsigned long requestInterval = 30*1000; // delay between requests; 30 seconds
*   boolean requested;                     // whether you've made a request since connecting
*   unsigned long lastAttemptTime = 0;     // last time you connected to the server, in milliseconds
**   int status = WL_IDLE_STATUS;
*   // if you don't want to use DNS (and reduce your sketch size)
*   // use the numeric IP instead of the name for the server:
*   //IPAddress server(74,125,232,128);  // numeric IP for Google (no DNS)
*   //byte mac[] = {0x90,0xA2,0xDA,0x0D,0x40,0x73};
*   //char server[] = "api.wunderground.com";    // name address for Google (using DNS)
*   IPAddress server (38,102,136,138); 
***   // Initialize the Ethernet client library
*   // with the IP address and port of the server 
*   // that you want to connect to (port 80 is default for HTTP):
*   WiFiClient client;
**   void setup() {
*     //Initialize serial and wait for port to open:
*     Serial.begin(9600);
*     pinMode(motorPin, OUTPUT); 
*     while (!Serial) {
*       ; // wait for serial port to connect. Needed for Leonardo only
*     }
**     // check for the presence of the shield:
*     if (WiFi.status() == WL_NO_SHIELD) {
*       Serial.println("WiFi shield not present"); 
*       // don't continue:
*       while(true);
*     } 
**     // attempt to connect to Wifi network:
*     while (status != WL_CONNECTED) { 
*       Serial.print("Attempting to connect to SSID: ");
*       Serial.println(ssid);
*       // Connect to WPA/WPA2 network. Change this line if using open or WEP network:    
*       status = WiFi.begin(ssid, pass);
*       //status = WiFi.begin(ssid);
*       // wait 10 seconds for connection:
*       delay(10000);
*     } 
*     Serial.println("Connected to wifi");
*     printWifiStatus();
*     connectToServer();
*   }
***   void loop() {
*     if (client.connected()) {
*       if (client.available()) {
*         char inChar = client.read();
*         //Serial.write(inChar);
*         currentLine += inChar; 
**         // if you get a newline, clear the line:
*         if (inChar == '\n') {
*           currentLine = "";
*         } 
*         // if the current line ends with <wind_mph>, it will
*         // be followed by the windspeed
*         if ( currentLine.endsWith("<wind_mph>")) {
*           // tweet is beginning. Clear the tweet string:
*           readingWind = true; 
*           wind = "";
*         }
*         // if you're currently reading the bytes of a windspeed,
*         // add them to the wind String:
*         if (readingWind) {
*           if (inChar != '<') {
*             wind += inChar;
*           } 
*           else {
*             // if you got a "<" character,
*             // you've reached the end of the statement:
*             readingWind = false;
*             //Serial.println("wind");
*             Serial.println(wind);
*             String windA = wind;
*             windA.replace(">","");
*             //Serial.println("windA");
*             Serial.println(windA);
*             int n;
*             char windSpeed[3];
*             windA.toCharArray(windSpeed, 3);
*             n = atoi(windSpeed); 
*             Serial.println("windteger:");
*             Serial.println(n);
*             //Serial.println("double windteger:");
*             //Serial.println(n*2);
*             // close the connection to the server:
**             int windN;
*             windN = map(n, 0, 60, 80, 255);
*             analogWrite(motorPin, windN);
*             Serial.println("Mapped Value Speed");
*             Serial.println(windN);
**             client.stop();
*           }
*         }
*       }
*     }
*     else if (millis() - lastAttemptTime > requestInterval) {
*       // if you're not connected, and two minutes have passed since
*       // your last connection, then attempt to connect again:
*       connectToServer();
*     }
*   }
**   void connectToServer(){  
*     Serial.println("\nStarting connection to server...");
*     // if you get a connection, report back via serial:
*     if (client.connect(server, 80)) {
*       Serial.println("connected to server");
*       // Make a HTTP request:
*       //client.println("GET /api/f109647c296273ca/geolookup/conditions/q/PA/Philadelphia.xml  HTTP/1.1");
*       client.println(GETRequest);
*       client.println("Host: api.wunderground.com");
*       Serial.println("Host: api.wunderground.com");
*       client.println("Connection: close");
*       Serial.println("Connection: close");
*       client.println();
*     }
*     lastAttemptTime = millis();
*   }
***   // if the server's disconnected, stop the client:
*   // if (!client.connected()) {
*   // Serial.println();
*   //Serial.println("disconnecting from server.");
*   // client.stop();
**   // do nothing forevermore:
*   //Swhile(true);
****   void printWifiStatus() {
*     // print the SSID of the network you're attached to:
*     Serial.print("SSID: ");
*     Serial.println(WiFi.SSID());
**     // print your WiFi shield's IP address:
*     IPAddress ip = WiFi.localIP();
*     Serial.print("IP Address: ");
*     Serial.println(ip);
**     // print the received signal strength:
*     long rssi = WiFi.RSSI();
*     Serial.print("signal strength (RSSI):");
*     Serial.print(rssi);
*     Serial.println(" dBm");
*   }
*

It's alive!!

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1409712141598_IMG_20140902_222619.jpg)

process shot montage

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1409853167827_process-photos.jpg)

I had read that the Arduino isn't great at supplying power to motors, but actually learning this now through experience where I can only get my fan to make a pathetic "whrrrrrrrr".   Max helped me come up with a schematic to use an external power supply, some transistors, diodes, and resistors to create a better, more well powered connection.  

These online sources were also helpful in figuring out the parts I needed as well.

[](http://medialappi.net/lab/tutorials/controlling-12-v-fan-with-arduino-digital-pin/)[http://medialappi.net/lab/tutorials/controlling-12-v-fan-with-arduino-digital-pin/](http://medialappi.net/lab/tutorials/controlling-12-v-fan-with-arduino-digital-pin/)

[](http://arduino-for-beginners.blogspot.com/2011/04/controlling-12v-fan-speed-with-pwm.html)[http://arduino-for-beginners.blogspot.com/2011/04/controlling-12v-fan-speed-with-pwm.html](http://arduino-for-beginners.blogspot.com/2011/04/controlling-12v-fan-speed-with-pwm.html)

[](http://makerfamily.wordpress.com/tag/mosfet-transistor-bipolar-power-control-speed-fan-arduino-darlingotn/)[http://makerfamily.wordpress.com/tag/mosfet-transistor-bipolar-power-control-speed-fan-arduino-darlingotn/](http://makerfamily.wordpress.com/tag/mosfet-transistor-bipolar-power-control-speed-fan-arduino-darlingotn/)

[](http://www.instructables.com/id/Use-Arduino-with-TIP120-transistor-to-control-moto/)[http://www.instructables.com/id/Use-Arduino-with-TIP120-transistor-to-control-moto/](http://www.instructables.com/id/Use-Arduino-with-TIP120-transistor-to-control-moto/)

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1407248659330_IMG_20140805_102244_463.jpg)

Max also enlightened me to the wonderful world of colored markers.

Glad this guy is still in action.

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1407525314068_THISGUY.jpg)

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1407525910810_THISGUYA copy.jpg)

**Items Purchased**

7/24 Red Oak Board 1' x 7' = 35.00 

7/24 WiFi Shield + Fans - SparkFun = 100.44

8/5 Radio Shack - Transistors/Regulators/Diodes/Fan = 39.31

*   Radio Shack - DC 12V Power supply
*   Adafruit - GPS Shield
*   Adafruit - Motor Shield
*   Adafruit - Servo Motors x 2
*   Adafruit GPS Antenna

**Python Beautiful Soup/Parsing**

Still trying to do the meteor/fireball project of scraping the site using Python.  Last night I got python on my computer and was able to download all the links to a text file - now I need to figure out how to download all the links as movie files - with the further intention of using RazPi and a small monitor in a sculpture.  Resources on this are quite scarce (lame).  

For future reference - here's a lot of links that talk about it:

[](http://www.pyimagesearch.com/2014/03/24/building-pokedex-python-scraping-pokemon-sprites-step-2-6/)http://www.pyimagesearch.com/2014/03/24/building-pokedex-python-scraping-pokemon-sprites-step-2-6/

[](http://stackoverflow.com/questions/13137817/how-to-download-image-using-requests)http://stackoverflow.com/questions/13137817/how-to-download-image-using-requests

[](https://github.com/NFicano/pytube)https://github.com/NFicano/pytube

[](http://www.techniqal.com/blog/2008/07/31/python-file-read-write-with-urllib2/)http://www.techniqal.com/blog/2008/07/31/python-file-read-write-with-urllib2/

[](http://stackoverflow.com/questions/14114729/save-a-file-using-the-python-requests-library)http://stackoverflow.com/questions/14114729/save-a-file-using-the-python-requests-library

[](https://docs.python.org/2/library/datetime.html)https://docs.python.org/2/library/datetime.html

[](https://pythonadventures.wordpress.com/tag/url/)https://pythonadventures.wordpress.com/tag/url/

[](http://urlgrabber.baseurl.org/)http://urlgrabber.baseurl.org/

********

OMG this one.  And _Hackers_ entering the Gibson reference.  Amazing

[](http://brianabelson.com/open-news/2013/12/17/scrape-the-gibson.html)http://brianabelson.com/open-news/2013/12/17/scrape-the-gibson.html

*

[](https://www.youtube.com/watch?v=vYNnPx8fZBs)https://www.youtube.com/watch?v=vYNnPx8fZBs

********  

*   **LINKS FOR LEARNING PYTHON SCRAPING**

[](http://stackoverflow.com/questions/19602931/basic-http-file-downloading-and-saving-to-disk-in-python)http://stackoverflow.com/questions/19602931/basic-http-file-downloading-and-saving-to-disk-in-python

[](http://stackoverflow.com/questions/3042757/downloading-a-picture-via-urllib-and-python)http://stackoverflow.com/questions/3042757/downloading-a-picture-via-urllib-and-python

convert avi files

[](http://askubuntu.com/questions/83161/use-ffmpeg-to-transform-mp4-to-same-high-quality-avi-file)[http://askubuntu.com/questions/83161/use-ffmpeg-to-transform-mp4-to-same-high-quality-avi-file](http://askubuntu.com/questions/83161/use-ffmpeg-to-transform-mp4-to-same-high-quality-avi-file)

[](https://github.com/atlex/ffmpeg-python)[https://github.com/atlex/ffmpeg-python](https://github.com/atlex/ffmpeg-python)

[](http://ubuntuforums.org/showthread.php?t=1031272)[http://ubuntuforums.org/showthread.php?t=1031272](http://ubuntuforums.org/showthread.php?t=1031272)

[](http://www.dkvermalinux.in/2012/01/python-script-for-video-converter-using.html)[http://www.dkvermalinux.in/2012/01/python-script-for-video-converter-using.html](http://www.dkvermalinux.in/2012/01/python-script-for-video-converter-using.html)

[](http://bjola.ca/tips-tools/quick-video-compression/)[http://bjola.ca/tips-tools/quick-video-compression/](http://bjola.ca/tips-tools/quick-video-compression/)

[](http://roshanbook.wordpress.com/2012/02/01/ffmpeg-cheat-sheet/)[http://roshanbook.wordpress.com/2012/02/01/ffmpeg-cheat-sheet/](http://roshanbook.wordpress.com/2012/02/01/ffmpeg-cheat-sheet/)

[](https://pypi.python.org/pypi/PIMS/0.2)[https://pypi.python.org/pypi/PIMS/0.2](https://pypi.python.org/pypi/PIMS/0.2)

PI

[](http://www.raspberrypi.org/forums/viewtopic.php?t=43880)[http://www.raspberrypi.org/forums/viewtopic.php?t=43880](http://www.raspberrypi.org/forums/viewtopic.php?t=43880)

[](http://www.cyberciti.biz/faq/howto-ffmpeg-avi-to-mov-video-converter/)[http://www.cyberciti.biz/faq/howto-ffmpeg-avi-to-mov-video-converter/](http://www.cyberciti.biz/faq/howto-ffmpeg-avi-to-mov-video-converter/)

combine files

[](http://stackoverflow.com/questions/17337260/how-to-merge-two-video-parts-and-get-a-playable-video-file-using-python)[http://stackoverflow.com/questions/17337260/how-to-merge-two-video-parts-and-get-a-playable-video-file-using-python](http://stackoverflow.com/questions/17337260/how-to-merge-two-video-parts-and-get-a-playable-video-file-using-python)

[](http://stackoverflow.com/questions/17311708/how-to-join-two-video-files-using-python)[http://stackoverflow.com/questions/17311708/how-to-join-two-video-files-using-python](http://stackoverflow.com/questions/17311708/how-to-join-two-video-files-using-python)

[](https://www.daniweb.com/software-development/python/threads/459079/how-to-merge-video-files-in-python)[https://www.daniweb.com/software-development/python/threads/459079/how-to-merge-video-files-in-python](https://www.daniweb.com/software-development/python/threads/459079/how-to-merge-video-files-in-python)

[](http://zulko.github.io/blog/2013/09/27/read-and-write-video-frames-in-python-using-ffmpeg/)[http://zulko.github.io/blog/2013/09/27/read-and-write-video-frames-in-python-using-ffmpeg/](http://zulko.github.io/blog/2013/09/27/read-and-write-video-frames-in-python-using-ffmpeg/)

******

*   **CODE**

Okey dokey - this script from Python gets the links to all of the .avi files from the desired webpage and writes them to a text file.

Things to figure out

*   how to download [avi] files

*   how to write the code so that it updates the webpage each day (webpage follows a year/month/day protocol - when its not 2AM I can figure this out

*   how to use either processing or razPi to compile videos into one

*   how to link this with razPi and send to a video screen

*   how to apply filterz

Downloads!!!!!

*   import requests
*   import urllib2
*   import urllib
*   from pprint import pprint
*   from urlparse import urljoin
*   from bs4 import BeautifulSoup
*   from urlparse import urljoin
*   import re
*   from subprocess import call
*   import time
*   print (time.strftime("%d/%m/%Y"))
**   DAY = (time.strftime("%d"))
*   MONTH = (time.strftime("%m"))
*   YEAR = (time.strftime("%Y"))
*   values = (YEAR, MONTH, DAY)
*   todayDATE = ''.join(values)
*   print todayDATE
**   webPage = ''.join('[](http://fireballs.ndc.nasa.gov/)http://fireballs.ndc.nasa.gov/' + todayDATE + '.html')
*   print webPage
*   #tell server you arent a scraper!
*   page = requests.get(webPage, headers={'User-agent':'Mozilla/5.0'}).text
*   #page = requests.get('[](http://fireballs.ndc.nasa.gov/20140827.html)http://fireballs.ndc.nasa.gov/20140827.html', headers={'User-agent':'Mozilla/5.0'}).text
*   basePage = "[](http://fireballs.ndc.nasa.gov/)http://fireballs.ndc.nasa.gov/"
*   soup = BeautifulSoup(page)
**   outfile = open('AVIfiles.txt','w')
**   tags = soup.findAll("a")
*   #just find files in links that end with .avi
*   tags = soup.findAll(href=re.compile(".avi"))
*   for tug in tags:
*           tug = tug.get('href')
*           #make absolute link
*           DL = urljoin(basePage, tug)
*           print DL
*           #write to file
*           outfile.write(DL + '\n')
**           
*   outfile.close()
*   #access file on computer for list of download options
*   input_file = open('AVIfiles.txt','r')
**   URL = input_file.read()
*   #get rid of spaces between lines
*   lines = URL.split()
*   print "Starting Download"
*   # Loop and display each line.
*   #lines = ['[](http://fireballs.ndc.nasa.gov/events/20140830/ev_20140830_033421A_01A.avi)http://fireballs.ndc.nasa.gov/events/20140830/ev_20140830_033421A_01A.avi', '[](http://fireballs.ndc.nasa.gov/events/20140830/ev_20140830_033421A_02A.avi)http://fireballs.ndc.nasa.gov/events/20140830/ev_20140830_033421A_02A.avi', '[](http://fireballs.ndc.nasa.gov/events/20140830/ev_20140830_033420A_03A.avi)http://fireballs.ndc.nasa.gov/events/20140830/ev_20140830_033420A_03A.avi', '[](http://fireballs.ndc.nasa.gov/events/20140830/ev_20140830_043053A_15A.avi)http://fireballs.ndc.nasa.gov/events/20140830/ev_20140830_043053A_15A.avi']
*   images = []
*   for line in lines:
*       IMAGE = line.rsplit("/",1)[1]
*       images.append(IMAGE)
*       urllib.urlretrieve(line, IMAGE)
**   ffmpeg_exec = "ffmpeg"
*   file_list = '|'.join(images)
*   ffmpeg_flags =  "-i concat:" + file_list + " -vcodec copy -acodec copy -y output.avi"
*   command = (ffmpeg_exec + " " + ffmpeg_flags).split();
*   call(command)
**   print "Download Complete" 

This code now uses the current date (since the webpage is updated daily based on the date) to scrape the links for all the files and then downloads them to the hard-drive and combines all the files into one .avi file which is then run through Processing to do this....

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_U6S0z289e3C_p.188779_1410926874307_undefined)

David helped me do the coding for piping in FFMPEG (video streamer) to do combining of the videos.  That jumped me forward about two weeks in the process.  THANK YOU SENSOR TEAM!

Next steps - learn how to automate this process and import everything to a raspberry pi and my website.

<s>This is what is returned in both the console and text file (all are legit links:</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_061041A_05A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_061041A_05A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_061041A_06A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_061041A_06A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_082051A_05A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_082051A_05A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_082051A_06A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_082051A_06A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_082050A_10A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_082050A_10A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_082050A_11A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_082050A_11A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_093828A_05A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_093828A_05A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_093828A_06A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_093828A_06A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_101514A_05A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_101514A_05A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_101513A_10A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_101513A_10A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_101513A_11A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_101513A_11A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_111047A_10A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_111047A_10A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_111047A_11A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_111047A_11A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_114039A_05A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_114039A_05A.avi</s>

[](http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_114039A_06A.avi)<s>http://fireballs.ndc.nasa.gov/events/20140901/ev_20140901_114039A_06A.avi</s>

**Mountain Water Compass **

I got the first section of code that I need working.  It measures the distance between two coordinates and returns a value in KM, and the cardinal direction needed to travel to that point.

The cardinal direction piece will help influence the servo motor in which direction it needs to turn.

Next steps are learning how to parse a csv file with arduino so I can have the program return the closest body of water and closest mountain.  

**   #include <TinyGPS++.h>
*   #include <SoftwareSerial.h>
*   /*
*      This sample code demonstrates the normal use of a TinyGPS++ (TinyGPSPlus) object.
*    It requires the use of SoftwareSerial, and assumes that you have a
*    4800-baud serial GPS device hooked up on pins 4(rx) and 3(tx).
*    */
*   static const int RXPin = 8, TXPin = 7;
*   static const uint32_t GPSBaud = 9600;
**   // The TinyGPS++ object
*   TinyGPSPlus gps;
**   // The serial connection to the GPS device
*   SoftwareSerial ss(RXPin, TXPin);
**   void setup()
*   {
*     Serial.begin(115200);
*     ss.begin(GPSBaud);
*   }
**   void loop(){
**     const double b_LAT = 37.7749295;
*     const double b_LON = -122.41941550000001;
*     double distanceKm =(unsigned long)TinyGPSPlus::distanceBetween( gps.location.lat(), gps.location.lng(),b_LAT, b_LON)/1000;
*     double courseTo = TinyGPSPlus::courseTo(gps.location.lat(), gps.location.lng(),b_LAT, b_LON);
**     Serial.print("Latitude");    
*     Serial.print (gps.location.lat());
*     Serial.print("Longitude");
*     Serial.print (gps.location.lng());
*     Serial.print("\nDistance (km) to SF: ");
*     Serial.println(distanceKm);
*     Serial.print("Course to SF: ");
*     Serial.println(courseTo);
*     Serial.print("Human directions: ");
*     Serial.println(TinyGPSPlus::cardinal(courseTo));
*     smartDelay (5000);
*     if (millis() > 5000 && gps.charsProcessed() < 10)
*       Serial.println(F("No GPS data received: check wiring"));
***   }
**   static void smartDelay(unsigned long ms)
*   {
*     unsigned long start = millis();
*     do 
*     {
*       while (ss.available())
*         gps.encode(ss.read());
*     } 
*     while (millis() - start < ms);
*   }
**   static void printFloat(float val, bool valid, int len, int prec)
*   {
*     if (!valid)
*     {
*       while (len-- > 1)
*         Serial.print('*');
*       Serial.print(' ');
*     }
*     else
*     {
*       Serial.print(val, prec);
*       int vi = abs((int)val);
*       int flen = prec + (val < 0.0 ? 2 : 1); // . and -
*       flen += vi >= 1000 ? 4 : vi >= 100 ? 3 : vi >= 10 ? 2 : 1;
*       for (int i=flen; i<len; ++i)
*         Serial.print(' ');
*     }
*     smartDelay(0);
*   }
**   static void printInt(unsigned long val, bool valid, int len)
*   {
*     char sz[32] = "*****************";
*     if (valid)
*       sprintf(sz, "%ld", val);
*     sz[len] = 0;
*     for (int i=strlen(sz); i<len; ++i)
*       sz[i] = ' ';
*     if (len > 0) 
*       sz[len-1] = ' ';
*     Serial.print(sz);
*     smartDelay(0);
*   }
**   static void printDateTime(TinyGPSDate &d, TinyGPSTime &t)
*   {
*     if (!d.isValid())
*     {
*       Serial.print(F("********** "));
*     }
*     else
*     {
*       char sz[32];
*       sprintf(sz, "%02d/%02d/%02d ", d.month(), d.day(), d.year());
*       Serial.print(sz);
*     }
**     if (!t.isValid())
*     {
*       Serial.print(F("******** "));
*     }
*     else
*     {
*       char sz[32];
*       sprintf(sz, "%02d:%02d:%02d ", t.hour(), t.minute(), t.second());
*       Serial.print(sz);
*     }
**     printInt(d.age(), d.isValid(), 5);
*     smartDelay(0);
*   }
**   static void printStr(const char *str, int len)
*   {
*     int slen = strlen(str);
*     for (int i=0; i<len; ++i)
*       Serial.print(i<slen ? str[i] : ' ');
*     smartDelay(0);
*   }
*

**GPS Distance to Mountain Parser**

The code for this part is working.  It compares a list of coordinates to your relative position and gives you the closest one back.  This current list only has three.  Next step after this: Figuring out north with a compass and turning stepper motors to the correct position based on the cardinal direction provided.... 

*   #include <TinyGPS++.h>
*   #include <SoftwareSerial.h>
*   #define chipSelect 10
*   double prevDist;
*   double distanceKm;
*   double newDistanceKm;
*   double mtnLat;
*   double mtnLon;
*   String mtnCardinal = "";
**   static const int RXPin = 8, TXPin = 7;
*   static const uint32_t GPSBaud = 9600;
**   // The TinyGPS++ object
*   TinyGPSPlus gps;
**   // The serial connection to the GPS device
*   SoftwareSerial ss(RXPin, TXPin);
*   float mat[15][2] = {
*     {
*       39.786009, -79.176802      }
*     ,
*     {
*       40.288958, -78.562966      }
*     ,
*     {
*       40.023446, -79.31045      }
*     ,
*     {
*       40.322408, -78.559467      }
*     ,
*     {
*       40.28158, -78.652144      }
*     ,
*     {
*       41.715166, -75.560916      }
*     ,
*     {
*       41.791517, -75.455872      }
*     ,
*     {
*       40.734982, -78.331218      }
*     ,
*     {
*       41.319458, -76.554559      }
*     ,
*     {
*       41.784398, -77.889033      }
*     ,
*     {
*       41.308695, -76.310813      }
*     ,
*     {
*       41.657509, -77.503034      }
*     ,
*     {
*       41.884043, -78.206051      }
*     ,
*     {
*       41.361448, -76.271802      }
*     ,
*     {
*       39.950138, -77.937133      }
**   };
**   void setup()
*   {
*     Serial.begin(115200);
*     ss.begin(GPSBaud);
*     //distanceKm = 0.0;
*     prevDist = 0.0;
*     //newDistanceKm = 0.0;
*   }
**   void loop(){
**     //const double b_LAT = 41.715166; 
*     //const double b_LON = -75.560916;
*     //double distanceKm =(unsigned long)TinyGPSPlus::distanceBetween( gps.location.lat(), gps.location.lng(),b_LAT, b_LON)/1000;
*     //double courseTo = TinyGPSPlus::courseTo(gps.location.lat(), gps.location.lng(),b_LAT, b_LON);
**     Serial.print("Latitude");    
*     Serial.print (gps.location.lat(),6);
*     Serial.println(",");
*     Serial.print("Longitude");
*     Serial.print (gps.location.lng(),6);
*     while(gps.location.lat()!=0.0 && gps.location.lng()!= 0.0){
*       Serial.println("\nDistance (km) to closest Mountain Program ");
*       prevDist = 1000.00;
*       for (int i=0; i<15; i++){
*         //distanceKm = 0.0;
*         float b_LAT = mat[i][0];
*         float b_LON = mat[i][1];
*         //prevDist = newDistanceKm;
*         double distanceKm =(unsigned long)TinyGPSPlus::distanceBetween( gps.location.lat(), gps.location.lng(),b_LAT, b_LON)/1000;
*         newDistanceKm = distanceKm;
*         //Serial.println("Comparing now");
*         //Serial.println("Previous Distance");
*         //Serial.println (prevDist);
*         //Serial.println("Current Distance");
*         //Serial.println (newDistanceKm);
*         if (newDistanceKm < prevDist && prevDist != 0){
*           mtnLat = b_LAT;
*           mtnLon = b_LON;
*           prevDist = distanceKm;
*         }
*         else {
*         }
*       }
**       Serial.println("Comparing ended");
*       //Serial.print("Distance to Mountain");
*       //Serial.println(newDistanceKm);
*       Serial.print("Distance to Mountain(km):");
*       Serial.println(prevDist);
**       Serial.println("Coordinates to the closest Mountain");
*       Serial.print(mtnLat, 6);
*       Serial.print(",");
*       Serial.println(mtnLon, 6);
*       double courseTo = TinyGPSPlus::courseTo(gps.location.lat(), gps.location.lng(),mtnLat, mtnLon);
*       String mtnCardinal = TinyGPSPlus::cardinal(courseTo);
*       Serial.println ("Cardinal Direction to Mtn");
*       Serial.println (mtnCardinal);
*       delay(10000);
*     }
*     //Serial.println(distanceKm);
*     // Serial.print("Course to SF: ");
*     // Serial.println(courseTo);
*     // Serial.print("Human directions: ");
*     // Serial.println(TinyGPSPlus::cardinal(courseTo));
*     smartDelay (5000);
*     if (millis() > 5000 && gps.charsProcessed() < 10)
*       Serial.println(F("No GPS data received: check wiring"));
***   }
**   static void smartDelay(unsigned long ms)
*   {
*     unsigned long start = millis();
*     do 
*     {
*       while (ss.available())
*         gps.encode(ss.read());
*     } 
*     while (millis() - start < ms);
*   }
**   static void printFloat(float val, bool valid, int len, int prec)
*   {
*     if (!valid)
*     {
*       while (len-- > 1)
*         Serial.print('*');
*       Serial.print(' ');
*     }
*     else
*     {
*       Serial.print(val, prec);
*       int vi = abs((int)val);
*       int flen = prec + (val < 0.0 ? 2 : 1); // . and -
*       flen += vi >= 1000 ? 4 : vi >= 100 ? 3 : vi >= 10 ? 2 : 1;
*       for (int i=flen; i<len; ++i)
*         Serial.print(' ');
*     }
*     smartDelay(0);
*   }
**   static void printInt(unsigned long val, bool valid, int len)
*   {
*     char sz[32] = "*****************";
*     if (valid)
*       sprintf(sz, "%ld", val);
*     sz[len] = 0;
*     for (int i=strlen(sz); i<len; ++i)
*       sz[i] = ' ';
*     if (len > 0) 
*       sz[len-1] = ' ';
*     Serial.print(sz);
*     smartDelay(0);
*   }
**   static void printDateTime(TinyGPSDate &d, TinyGPSTime &t)
*   {
*     if (!d.isValid())
*     {
*       Serial.print(F("********** "));
*     }
*     else
*     {
*       char sz[32];
*       sprintf(sz, "%02d/%02d/%02d ", d.month(), d.day(), d.year());
*       Serial.print(sz);
*     }
**     if (!t.isValid())
*     {
*       Serial.print(F("******** "));
*     }
*     else
*     {
*       char sz[32];
*       sprintf(sz, "%02d:%02d:%02d ", t.hour(), t.minute(), t.second());
*       Serial.print(sz);
*     }
**     printInt(d.age(), d.isValid(), 5);
*     smartDelay(0);
*   }
**   static void printStr(const char *str, int len)
*   {
*     int slen = strlen(str);
*     for (int i=0; i<len; ++i)
*       Serial.print(i<slen ? str[i] : ' ');
*     smartDelay(0);
*   }

**COMPASS/Stepper Motor Set**

Getting the digital compass/magnetometer to set the stepper motor at North 

Works - but I still need to account for the magnetic fields of the stepper motors. 

This runs in setup - currently works with just one motor - I'll get it on two on Thursday. 

*   #include <Wire.h>
*   #include <Adafruit_Sensor.h>
*   #include <Adafruit_HMC5883_U.h>
*   #include <Adafruit_MotorShield.h>
*   #include "utility/Adafruit_PWMServoDriver.h"
*   Adafruit_MotorShield AFMS = Adafruit_MotorShield(); 
*   // Or, create it with a different I2C address (say for stacking)
*   // Adafruit_MotorShield AFMS = Adafruit_MotorShield(0x61); 
**   // Connect a stepper motor with 200 steps per revolution (1.8 degree)
*   // to motor port #2 (M3 and M4)
*   Adafruit_StepperMotor *myMotor = AFMS.getStepper(200, 1);
*   //Adafruit_StepperMotor *myMotorA = AFMS.getStepper(200, 1);
**   /* Assign a unique ID to this sensor at the same time */
*   Adafruit_HMC5883_Unified mag = Adafruit_HMC5883_Unified(12345);
*   int sensorPin = A3;    // select the input pin for the potentiometer
*   int sensorValue = 0;
*   boolean goNorth = false;
***   void setup(){
*     Serial.begin(9600);
**     /* Initialise the sensor */
**     AFMS.begin();  // create with the default frequency 1.6KHz
*     //AFMS.begin(1000);  // OR with a different frequency, say 1KHz
**     myMotor->setSpeed(5);  // 10 rpm
*     //myMotorA->setSpeed(100); 
*     !mag.begin();
*     while(goNorth == false){
*       northTest();
*     }
****   }
*   void loop(){
*    
*   }
**   void northTest() 
*   {
*     /* Get a new sensor event */
*     sensors_event_t event; 
*     mag.getEvent(&event);
*     float heading = atan2(event.magnetic.y, event.magnetic.x);
**     float declinationAngle = 0.2;
*     heading += declinationAngle;
**     if(heading < 0)
*       heading += 2*PI;
**     if(heading > 2*PI)
*       heading -= 2*PI;
*     float headingDegrees = heading * 180/M_PI; 
*     Serial.print("Heading (degrees): "); 
*     Serial.println(headingDegrees);
*     delay(1000);
*     if (headingDegrees < 4.0 || headingDegrees > 356.0){
*       Serial.println("North");
*       setNorth();
*     }
*     else{
*     }
*     Serial.println("Done");
***   }
**   void setNorth(){
*     sensorValue = analogRead(sensorPin);
*     if (sensorValue > 0){
*           Serial.println("Rotating"); 
*       Serial.println(sensorValue);
*       myMotor->setSpeed(2);
*       myMotor->step(1, FORWARD, MICROSTEP); 
*     }
*     else {
*       myMotor->release();
*       Serial.println("North Declared");
*       goNorth=true;
*     }
*   }

hey jacob, you need to start posting your stuff to github! :) -Lee

I will once all the code is finished!

**Complete code for "Compass for mountain and water code"**

Still a little in shock that this works.  

Compiles to:  Binary sketch size: 21,878 bytes (of a 32,256 byte maximum)

I might try to add in more data points, maybe top 50 largest bodies of water and highest points so it is a more robust work.

**   <u>#include <TinyGPS++.h></u>
*   <u>#include <SoftwareSerial.h></u>
*   <u>#include <Wire.h></u>
*   <u>#include <Adafruit_MotorShield.h></u>
*   <u>#include "utility/Adafruit_PWMServoDriver.h"</u>
*   <u>#include <Adafruit_Sensor.h></u>
*   <u>#include <Adafruit_HMC5883_U.h></u>
*   <u>//#define chipSelect 10</u>
*   <u>static const int RXPin = 8, TXPin = 7;</u>
*   <u>static const uint32_t GPSBaud = 9600;</u>
*   <u>double saveLat;</u>
*   <u>double saveLon;</u>
*   <u>double saveLata;</u>
*   <u>double saveLona;</u>
*   <u>float degVal = 0;</u>
*   <u>float North = 0.0;</u>
*   <u>int stepVal;</u>
*   <u>int newVal;</u>
*   <u>int oldVal;</u>
*   <u>int newValDeg;</u>
*   <u>int stepValA;</u>
*   <u>int newValA;</u>
*   <u>int oldValA;</u>
*   <u>int newValDegA;</u>
*   <u>int sensorPin = A1;    // select the input pin for the potentiometer</u>
*   <u>int sensorValue = 0;</u>
*   <u>boolean goNorth = false;</u>
*   <u>int sensorPinA = A2;    // select the input pin for the potentiometer</u>
*   <u>int sensorValueA = 0;</u>
*   <u>boolean goNorthA = false;</u>
**   <u>Adafruit_MotorShield AFMS = Adafruit_MotorShield(); </u>
*   <u>Adafruit_StepperMotor *myMotor = AFMS.getStepper(200, 2);</u>
*   <u>Adafruit_StepperMotor *myMotorA = AFMS.getStepper(200, 1);</u>
*   <u>Adafruit_HMC5883_Unified mag = Adafruit_HMC5883_Unified(12345);</u>
***   <u>// The TinyGPS++ object</u>
*   <u>TinyGPSPlus gps;</u>
*   <u>// The serial connection to the GPS device</u>
*   <u>SoftwareSerial ss(RXPin, TXPin);</u>
*   <u>float water [15][2] = {</u>
*   <u>  {</u>
*   <u>    42.173801, -79.9892381                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.9744187, -78.9373099                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.5923208, -80.5160608                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    40.8596101, -75.6164442                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    40.4619296, -75.2289452                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    40.9495984, -80.0150423                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.9782029, -77.2018718                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.2333896, -80.44868                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.363333, -76.043889                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.4150111, -80.133088                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    40.0467459, -78.8522447                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.8136682, -79.8347748                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.0488459, -75.5873438                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.1110487, -75.456321                      }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    40.0216657, -78.8743569                      }</u>
*   <u>};</u>
*   <u>float mount[15][2] = {</u>
*   <u>  {</u>
*   <u>    39.786009, -79.176802                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    40.288958, -78.562966                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    40.023446, -79.31045                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    40.322408, -78.559467                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    40.28158, -78.652144                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.715166, -75.560916                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.791517, -75.455872                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    40.734982, -78.331218                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.319458, -76.554559                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.784398, -77.889033                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.308695, -76.310813                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.657509, -77.503034                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.884043, -78.206051                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    41.361448, -76.271802                            }</u>
*   <u>  ,</u>
*   <u>  {</u>
*   <u>    39.950138, -77.937133                            }</u>
**   <u>};</u>
**   <u>void setup()</u>
*   <u>{</u>
*   <u>  Serial.begin(115200);</u>
*   <u>  ss.begin(GPSBaud);</u>
*   <u>  AFMS.begin();  // create with the default frequency 1.6KHz</u>
*   <u>  //AFMS.begin(1000);  // OR with a different frequency, say 1KHz</u>
*   <u>  myMotorA->setSpeed(5);  // 10 rpm </u>
*   <u>  !mag.begin();</u>
*   <u>  while(goNorth == false){</u>
*   <u>    northTest(); </u>
*   <u>    //myMotorA->setSpeed(100);</u>
*   <u>  }</u>
*   <u>  while(goNorthA == false){</u>
*   <u>    northTestA();</u>
*   <u>  }</u>
*   <u>  myMotor->setSpeed(100);</u>
*   <u>  myMotorA->setSpeed(100);</u>
*   <u>}</u>
**   <u>void loop(){</u>
*   <u>  Serial.print("Satillites Available");</u>
*   <u>  Serial.println(gps.satellites.value());</u>
*   <u>  Serial.print("Latitude");    </u>
*   <u>  Serial.print (gps.location.lat(),6);</u>
*   <u>  Serial.print(",");</u>
*   <u>  Serial.print("Longitude");</u>
*   <u>  Serial.println (gps.location.lng(),6);</u>
*   <u>  while(gps.location.lat()!=0.0 && gps.location.lng()!= 0.0){</u>
**   <u>    findWaterDist();</u>
*   <u>    findMountDist();</u>
**   <u>    delay(10000);</u>
*   <u>  }</u>
*   <u>  smartDelay (5000);</u>
*   <u>  if (millis() > 5000 && gps.charsProcessed() < 10)</u>
*   <u>    Serial.println(F("No GPS data received: check wiring"));</u>
***   <u>}</u>
**   <u>static void smartDelay(unsigned long ms)</u>
*   <u>{</u>
*   <u>  unsigned long start = millis();</u>
*   <u>  do </u>
*   <u>  {</u>
*   <u>    while (ss.available())</u>
*   <u>      gps.encode(ss.read());</u>
*   <u>  } </u>
*   <u>  while (millis() - start < ms);</u>
*   <u>}</u>
**   <u>static void printFloat(float val, bool valid, int len, int prec)</u>
*   <u>{</u>
*   <u>  if (!valid)</u>
*   <u>  {</u>
*   <u>    while (len-- > 1)</u>
*   <u>      Serial.print('*');</u>
*   <u>    Serial.print(' ');</u>
*   <u>  }</u>
*   <u>  else</u>
*   <u>  {</u>
*   <u>    Serial.print(val, prec);</u>
*   <u>    int vi = abs((int)val);</u>
*   <u>    int flen = prec + (val < 0.0 ? 2 : 1); // . and -</u>
*   <u>    flen += vi >= 1000 ? 4 : vi >= 100 ? 3 : vi >= 10 ? 2 : 1;</u>
*   <u>    for (int i=flen; i<len; ++i)</u>
*   <u>      Serial.print(' ');</u>
*   <u>  }</u>
*   <u>  smartDelay(0);</u>
*   <u>}</u>
**   <u>static void printInt(unsigned long val, bool valid, int len)</u>
*   <u>{</u>
*   <u>  char sz[32] = "*****************";</u>
*   <u>  if (valid)</u>
*   <u>    sprintf(sz, "%ld", val);</u>
*   <u>  sz[len] = 0;</u>
*   <u>  for (int i=strlen(sz); i<len; ++i)</u>
*   <u>    sz[i] = ' ';</u>
*   <u>  if (len > 0) </u>
*   <u>    sz[len-1] = ' ';</u>
*   <u>  Serial.print(sz);</u>
*   <u>  smartDelay(0);</u>
*   <u>}</u>
**   <u>static void printDateTime(TinyGPSDate &d, TinyGPSTime &t)</u>
*   <u>{</u>
*   <u>  if (!d.isValid())</u>
*   <u>  {</u>
*   <u>    Serial.print(F("********** "));</u>
*   <u>  }</u>
*   <u>  else</u>
*   <u>  {</u>
*   <u>    char sz[32];</u>
*   <u>    sprintf(sz, "%02d/%02d/%02d ", d.month(), d.day(), d.year());</u>
*   <u>    Serial.print(sz);</u>
*   <u>  }</u>
**   <u>  if (!t.isValid())</u>
*   <u>  {</u>
*   <u>    Serial.print(F("******** "));</u>
*   <u>  }</u>
*   <u>  else</u>
*   <u>  {</u>
*   <u>    char sz[32];</u>
*   <u>    sprintf(sz, "%02d:%02d:%02d ", t.hour(), t.minute(), t.second());</u>
*   <u>    Serial.print(sz);</u>
*   <u>  }</u>
**   <u>  printInt(d.age(), d.isValid(), 5);</u>
*   <u>  smartDelay(0);</u>
*   <u>}</u>
**   <u>static void printStr(const char *str, int len)</u>
*   <u>{</u>
*   <u>  int slen = strlen(str);</u>
*   <u>  for (int i=0; i<len; ++i)</u>
*   <u>    Serial.print(i<slen ? str[i] : ' ');</u>
*   <u>  smartDelay(0);</u>
*   <u>}</u>
***   <u>void findWaterDist(){</u>
*   <u>  Serial.println("\nDistance (km) to closest Water Program ");</u>
*   <u>  double prevDist = 1000.00;</u>
*   <u>  //double saveLat;</u>
*   <u>  //double saveLon;</u>
*   <u>  for (int i=0; i<15; i++){</u>
*   <u>    float b_LAT = water[i][0];</u>
*   <u>    float b_LON = water[i][1];</u>
*   <u>    double distanceKm =(unsigned long)TinyGPSPlus::distanceBetween( gps.location.lat(), gps.location.lng(),b_LAT, b_LON)/1000;</u>
*   <u>    double newDistanceKm = distanceKm;</u>
*   <u>    if (newDistanceKm < prevDist && prevDist != 0){</u>
*   <u>      saveLat = b_LAT;</u>
*   <u>      saveLon = b_LON;</u>
*   <u>      prevDist = distanceKm;</u>
*   <u>    }</u>
*   <u>    else {</u>
*   <u>    }</u>
**   <u>  }</u>
*   <u>  Serial.println("Comparing ended");</u>
*   <u>  Serial.print("Distance to Water(km):");</u>
*   <u>  Serial.println(prevDist);</u>
**   <u>  Serial.println("Coordinates to the closest Water");</u>
*   <u>  Serial.print(saveLat, 6);</u>
*   <u>  Serial.print(",");</u>
*   <u>  Serial.println(saveLon, 6);</u>
*   <u>  double courseTo = TinyGPSPlus::courseTo(gps.location.lat(), gps.location.lng(),saveLat, saveLon);</u>
*   <u>  //String newCardinal = "";</u>
*   <u>  Serial.println("Cardinal Degrees");</u>
*   <u>  Serial.println(courseTo);</u>
*   <u>  String newCardinal = TinyGPSPlus::cardinal(courseTo);</u>
*   <u>  Serial.println ("Cardinal Direction to Water");</u>
*   <u>  Serial.println (newCardinal);</u>
*   <u>  newValA = courseTo;</u>
*   <u>  int stepValA = abs(newValA - oldValA);</u>
*   <u>  //Serial.println(newValA);</u>
*   <u>  //Serial.println(oldValA);</u>
*   <u>  Serial.println(stepValA);</u>
*   <u>  if (newValA > oldValA){</u>
*   <u>    myMotorA->step((int(stepValA/1.8)), FORWARD, MICROSTEP);</u>
*   <u>    myMotorA->release();</u>
*   <u>    Serial.print("Forward:");</u>
*   <u>    Serial.println(int(stepValA/1.8));</u>
*   <u>    oldValA = newValA;</u>
*   <u>  }</u>
*   <u>  else if (newValA<oldValA){</u>
*   <u>    myMotorA->step((int(stepValA/1.8)), BACKWARD, MICROSTEP);</u>
*   <u>    myMotorA->release();</u>
*   <u>    Serial.print("Backward:");</u>
*   <u>    Serial.println(int(stepValA/1.8));  </u>
*   <u>    oldValA = newValA;</u>
*   <u>  }</u>
*   <u>  else if (newValA==oldValA){</u>
*   <u>    Serial.println("No Change in Direction");</u>
*   <u>  }</u>
*   <u>}</u>
**   <u>void findMountDist(){</u>
*   <u>  Serial.println("\nDistance (km) to closest Mountain Program ");</u>
*   <u>  double prevDist = 1000.00;</u>
*   <u>  //double saveLata;</u>
*   <u>  //double saveLona;</u>
*   <u>  for (int i=0; i<15; i++){</u>
*   <u>    float b_LAT = mount[i][0];</u>
*   <u>    float b_LON = mount[i][1];</u>
*   <u>    double distanceKm =(unsigned long)TinyGPSPlus::distanceBetween( gps.location.lat(), gps.location.lng(),b_LAT, b_LON)/1000;</u>
*   <u>    double newDistanceKm = distanceKm;</u>
*   <u>    if (newDistanceKm < prevDist && prevDist != 0){</u>
*   <u>      saveLata = b_LAT;</u>
*   <u>      saveLona = b_LON;</u>
*   <u>      prevDist = distanceKm;</u>
*   <u>    }</u>
*   <u>    else {</u>
*   <u>    }</u>
*   <u>  }</u>
**   <u>  Serial.println("Comparing ended");</u>
*   <u>  Serial.print("Distance to Mountain(km):");</u>
*   <u>  Serial.println(prevDist);</u>
**   <u>  Serial.println("Coordinates to the closest Mountain");</u>
*   <u>  Serial.print(saveLata, 6);</u>
*   <u>  Serial.print(",");</u>
*   <u>  Serial.println(saveLona, 6);</u>
*   <u>  double courseTo = TinyGPSPlus::courseTo(gps.location.lat(), gps.location.lng(),saveLata, saveLona);</u>
*   <u>  //String newCardinal = "";</u>
*   <u>  Serial.println("Cardinal Degrees");</u>
*   <u>  Serial.println(courseTo);</u>
*   <u>  String newCardinal = TinyGPSPlus::cardinal(courseTo);</u>
*   <u>  Serial.println ("Cardinal Direction to Mtn");</u>
*   <u>  Serial.println (newCardinal);</u>
*   <u>  //rotating motor</u>
*   <u>  newVal = courseTo;</u>
*   <u>  int stepVal = abs(newVal - oldVal);</u>
*   <u>  Serial.println(stepVal);</u>
*   <u>  if (newVal > oldVal){</u>
*   <u>    myMotor->step((int(stepVal/1.8)), FORWARD, MICROSTEP);</u>
*   <u>    myMotor->release();</u>
*   <u>    Serial.print("Forward:");</u>
*   <u>    Serial.println(int(stepVal/1.8));</u>
*   <u>    oldVal = newVal;</u>
*   <u>  }</u>
*   <u>  else if (newVal<oldVal){</u>
*   <u>    myMotor->step(int((stepVal/1.8)), BACKWARD, MICROSTEP);</u>
*   <u>    myMotor->release();</u>
*   <u>    Serial.print("Backward:");</u>
*   <u>    Serial.println(int(stepVal/1.8));  </u>
*   <u>    oldVal = newVal;</u>
*   <u>  }</u>
*   <u>  else if (newVal==oldVal){</u>
*   <u>    Serial.println("No Change in Direction");</u>
*   <u>  } </u>
*   <u>}</u>
**   <u>void northTest() </u>
*   <u>{</u>
*   <u>  /* Get a new sensor event */</u>
*   <u>  sensors_event_t event; </u>
*   <u>  mag.getEvent(&event);</u>
*   <u>  float heading = atan2(event.magnetic.y, event.magnetic.x);</u>
**   <u>  float declinationAngle = 0.2;</u>
*   <u>  heading += declinationAngle;</u>
**   <u>  if(heading < 0)</u>
*   <u>    heading += 2*PI;</u>
**   <u>  if(heading > 2*PI)</u>
*   <u>    heading -= 2*PI;</u>
*   <u>  float headingDegrees = heading * 180/M_PI; </u>
*   <u>  Serial.print("Heading (degrees): "); </u>
*   <u>  Serial.println(headingDegrees);</u>
*   <u>  delay(1000);</u>
*   <u>  if (headingDegrees < 4.0 || headingDegrees > 356.0){</u>
*   <u>    Serial.println("North");</u>
*   <u>    setNorth();</u>
*   <u>  }</u>
*   <u>  else{</u>
*   <u>  }</u>
*   <u>  Serial.println("Done");</u>
***   <u>}</u>
**   <u>void setNorth(){</u>
*   <u>  sensorValue = analogRead(sensorPin);</u>
*   <u>  if (sensorValue > 0){</u>
*   <u>    Serial.println("Rotating"); </u>
*   <u>    Serial.println(sensorValue);</u>
*   <u>    myMotor->setSpeed(2);</u>
*   <u>    myMotor->step(1, FORWARD, MICROSTEP); </u>
*   <u>  }</u>
*   <u>  else {</u>
*   <u>    myMotor->release();</u>
*   <u>    Serial.println("Motor 1 North Declared");</u>
*   <u>    goNorth=true;</u>
*   <u>  }</u>
*   <u>}</u>
*   <u>void northTestA() </u>
*   <u>{</u>
*   <u>  /* Get a new sensor event */</u>
*   <u>  sensors_event_t event; </u>
*   <u>  mag.getEvent(&event);</u>
*   <u>  float heading = atan2(event.magnetic.y, event.magnetic.x);</u>
**   <u>  float declinationAngle = 0.2;</u>
*   <u>  heading += declinationAngle;</u>
**   <u>  if(heading < 0)</u>
*   <u>    heading += 2*PI;</u>
**   <u>  if(heading > 2*PI)</u>
*   <u>    heading -= 2*PI;</u>
*   <u>  float headingDegrees = heading * 180/M_PI; </u>
*   <u>  Serial.print("Heading (degrees): "); </u>
*   <u>  Serial.println(headingDegrees);</u>
*   <u>  delay(1000);</u>
*   <u>  if (headingDegrees < 4.0 || headingDegrees > 356.0){</u>
*   <u>    Serial.println("North");</u>
*   <u>    setNorthA();</u>
*   <u>  }</u>
*   <u>  else{</u>
*   <u>  }</u>
*   <u>  Serial.println("Done");</u>
***   <u>}</u>
**   <u>void setNorthA(){</u>
*   <u>  sensorValueA = analogRead(sensorPinA);</u>
*   <u>  if (sensorValueA > 0){</u>
*   <u>    Serial.println("Rotating"); </u>
*   <u>    Serial.println(sensorValueA);</u>
*   <u>    myMotorA->setSpeed(2);</u>
*   <u>    myMotorA->step(1, FORWARD, MICROSTEP); </u>
*   <u>  }</u>
*   <u>  else {</u>
*   <u>    myMotorA->release();</u>
*   <u>    Serial.println("Motor 2 North Declared");</u>
*   <u>    goNorthA=true;</u>
*   <u>  }</u>
*   <u>}</u>
**

**Internal Deadlines**

Compass/Suitcase

11/14 - Compass for mountain and water complete

11/21 - Video completed for suitcase piece

Wish-booth

11/21 - Wishbooth construction complete

11/28 - Construct/re-construct test complete and finalized

Bike project

11/21 - Mostly Complete

11/28 - Totally Complete

Marathon

11/23 - Run a marathon, don't pass out.