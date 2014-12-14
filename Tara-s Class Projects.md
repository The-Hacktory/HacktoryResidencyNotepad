# Tara's Class Projects

**HOMEWORK 2**

Twitter naked dress: [](https://www.behance.net/gallery/17256769/xpose)http[s://www.behance.net/gallery/17256769/xpose](http://www.dailydot.com/technology/transparent-tweet-dress-privacy/)

Gesture texting hoodie: [](http://www.theverge.com/mobile/2014/6/8/5791464/finally-theres-a-hoodie-that-can-text-your-mom)http://www.theverge.com/mobile/2014/6/8/5791464/finally-theres-a-hoodie-that-can-text-your-mom

Sonic scarf: [](http://popkalab.com/orchestrascarf.html)http://popkalab.com/orchestrascarf.html

Image skirts: [](http://cutecircuit.com/collections/aw-14-15/)http://cutecircuit.com/collections/aw-14-15/

Code to put in void draw at the end to show mouse coordinates if you want to draw specifically at certain spots:

** //...to label coordinates on mouse**

**  frame.setTitle(mouseX + ", " + mouseY);**

  Follow the mouse, change color homework:

  int time1 = 2000;

int time2 = 4000;

float x = 0;

 void setup() {

 size(500, 500);

 smooth();

 stroke(1, 50);

}

 void draw() {

   background(255);

       if (keyPressed) {

      ellipse(250, 250, 250, 250);//ellipse pops up in the middle

      fill(0, 0, 255);//moving ellipse changes color

    }

    int currentTime = millis();//floats around, no  edge, moves offscreen in time

    if (currentTime > time2) {

      x -= 0.5;

 } else if (currentTime > time1) {

      x += 2;

 }

 float weight = dist(mouseX, mouseY, pmouseX, pmouseY); //ellipse floats around on its own

    translate(mouseX, mouseY); //moves ellipse around

    ellipse(x, 60, 90, 90);

    fill(255, 0, 0);//fills ellipse with red

 }

**HOMEWORK 1**

*   Angry Birds - so silly!
*   Learn about LOGO - enough to at least understand terminology a bit
*   Tutorial
*   Screenshot

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_IyAPaZeBlaR_p.188775_1402680217786_Screen Shot 2014-06-13 at 12.50.01 PM.png)

*   Video talk

**Lee's Questions To Ponder**

*   Was this easy/hard? _Easy._
*   What was the point of the Angry Birds code tutorial? _Intro to simple code concepts (repeats, if, else, etc.  more if you're totally new and take a look at coding layouts), creating movement whether it be a dot that's drawing or Mars Rover, etc.  Easy for kids, but also for people with no coding language vocabulary at all via intro to block coding. Introduction to LOGO in some ways or at least intro to graphical interface for programming._
*   Were you surprised by how quickly you made something in Processing? _Yes and no.  It brought back middle school commands on TSR80s.  Creating visuals, etc.  _
*   What do you like about coding in Processing? What do you find difficult? _Language functions creating visuals, opportunity to make mistakes, fail and problem solve. Using curly brackets and keyboards and new vocabulary. Difficulties are the "whys" and memorizing conventions. Also, imagining the next step, although I'm beginning to see the matrix in all of the programs we use now. _

From **Intro to 21st Century Processing **class, a laser cut skirt idea:

How to make cuts expand into 3D from 2D. Playing with the idea of flexi - inspired by lampshades like this: [](http://www.thingiverse.com/thing:289597)[http://www.thingiverse.com/thing:289597](http://www.thingiverse.com/thing:289597)

 And in wood: [](http://www.thingiverse.com/thing:56655)[http://www.thingiverse.com/thing:56655](http://www.thingiverse.com/thing:56655)