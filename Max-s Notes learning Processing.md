# Max's Notes learning Processing

**   _OMG. Shit is real. Ive been listening to lil kim's **big momma thing _**_on continous repeat for three days. That may tangentially explain why i've been using the Hackpad like its 1997 . Thanks Lee. - big maxie_

shadow puppets lee. 

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403032941820_IMG_4936.jpg)![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403032907242_Screen%20Shot%202014-06-07%20at%207.01.26%20PM.png)![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403032764592_Screen%20Shot%202014-05-28%20at%2012.27.25%20PM.png)/*

*    * Creative Coding
*    * Week 2, 03 - n squares
*    * by Indae Hwang and Jon McCormack
*    * Copyright (c) 2014 Monash University
*    *
*    * In the next iteration of the square drawing sketch, this version selects a random number of squares
*    * and a random gap between them. From this it calculates the width of each square then draws the squares
*    * using two nested for loops.
*    *
*    * A simple drop shadow is also drawn to give the illusion of depth.
*    * 
*    */
**   void setup() {
*     size(600, 600);
*     rectMode(CORNER); //could change to CENTER or RADIUS
*     noStroke();
*     frameRate(1);  // set the frame rate to 1 draw() call pegvr second
*     randomSeed(hour() + minute() + second() + millis()); // uses internal clock to generate random number
*   }
***   void draw() {
**     background(180); // clear the screen to grey
*     
*     //int num = (int) random(3, 12);   // select a random number of squares each frame
*    // int gap = (int) random(5, 50); // select a random gap between each square
*     
*     int num = 5; // define 5 by 5 grid
*     int gap = 15; // unifide spacing
*     
*     // calculate the size of each square for the given number of squares and gap between them
*     float cellsize = ( width - (num + 1) * gap ) / (float)num;
*     
*     // print out the size of each square
*     println("cellsize = " + cellsize);
*     
*     // calculate shadow offset
*     float offsetX = cellsize/16.0;
*     float offsetY = cellsize/16.0;
*    
*    
**   //initializing the variable outside of the loop
*       for (int i=0; i<num; i++) {
*         for (int j=0; j<num; j++) {
**           
*           
*           float op=random(1, 255); // generate random alpha
*           float w=random(-20, 20); // generate random offset 
*           
*           fill(w, op); // shadow
*           rect(gap * (i+1) + cellsize * i + offsetX + w, gap * (j+1) + cellsize * j + offsetY + w, cellsize, cellsize);
*           
*           fill(247, 57, 57, op); // rectangle
*           rect(gap * (i+1) + cellsize * i + w, gap * (j+1) + cellsize * j - w, cellsize, cellsize);
*           
*         println("i = ",i," j = ", j); 
*        println("opacity = ", op);
*       println("wobble = ", w); 
*       }// end for (j)
*        
*       }//end for (i)
*       if (keyPressed == true && key=='s') {
*       saveFrame("squares-####.jpg");
*     println("saved");} // to check that the key is working 
*       
*       
*   } //end of draw 
*

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403032389095_squares-0015.jpg)

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403032371008_squares-0004.jpg)![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403018732021_Screen%20Shot%202014-06-17%20at%2012.15.13%20AM.png)![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403018732017_Screen%20Shot%202014-06-17%20at%2012.15.07%20AM.png)![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403018732014_Screen%20Shot%202014-06-17%20at%2012.15.03%20AM.png)![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403018732011_Screen%20Shot%202014-06-17%20at%2012.13.05%20AM.png)

void setup() {  

size(600, 600);  

rectMode(CORNER);  

noStroke();  

randomSeed(0);  

frameRate(1);  

}

void draw() {

  //background(600);

for (int i=0; i < 600; i++) {  

float r = random(0, 255);  

stroke(r, r/i*r, r*i/i*i);  

quad(i, 0, i, 600, r*i, 600/r, (i+r)/600, i*(r*r));

}

}

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403018732004_Screen%20Shot%202014-06-16%20at%2010.23.52%20PM.png)

*   /*
*    * Creative Coding
*    * Week 2, 03 - n squares
*    * by Indae Hwang and Jon McCormack
*    * Copyright (c) 2014 Monash University
*    *
*    * In the next iteration of the square drawing sketch, this version selects a random number of squares
*    * and a random gap between them. From this it calculates the width of each square then draws the squares
*    * using two nested for loops.
*    *
*    * A simple drop shadow is also drawn to give the illusion of depth.
*    * 
*    */
**   void setup() {
*     size(600, 600);
*     rectMode(CORNER);
*     noStroke();
*     frameRate(1);  // set the frame rate to 1 draw() call per second
*   }
***   void draw() {
**     background(180); // clear the screen to grey
*     
*     int num = (int) random(3, 12);   // select a random number of squares each frame
*     int gap = (int) random(-50, 50); // select a random gap between each square
*     int wobble = (int) random(4, 50); // generate number for off seting squares
*     
*     // calculate the size of each square for the given number of squares and gap between them
*     float cellsize = ( width - (num + 1) * gap ) / (float)num;
*     
*     // print out the size of each square
*     println("cellsize = " + cellsize);
*     
*     // calculate shadow offset
*     float offsetX = cellsize/16.0;
*     float offsetY = cellsize/16.0;
*    
**       for (int i=0; i<num; i++) {
*         for (int j=0; j<num; j++) {
*           for (int w=0; w<num; w++){
*           //?create local variable so each square has a random function invoked 
*           //fill(140, 180); // shadow
*           //rect(gap * (i+1) + cellsize * i + offsetX, gap * (j+1) + cellsize * j + offsetY, cellsize, cellsize);
**           fill(247, 57, 57, 180); // rectangle
*           rect(gap * (i+1) + cellsize * i, gap  * (j+1) + cellsize * j, cellsize, cellsize);
*           // rect(x, y, width, height)
*           }
*         }
*       }
*       // save your drawing when you press keyboard 's'
*       // ?make a loop that generates a i++ for every new saved image
*       // ?to make sure it doesnt continue to overwrite the same image
*     if (keyPressed == true && key=='s') {
*       saveFrame("squares.jpg");
*     }
**     // erase your drawing when you press keyboard 'r'
*     if (keyPressed == true && key == 'r') {
*       background(0,0,255);
*     }
*   } //end of draw 
*

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403018680909_Screen%20Shot%202014-05-26%20at%206.41.55%20PM.png)

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403018681542_Screen%20Shot%202014-05-26%20at%203.46.50%20PM.png)

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403018680903_Screen%20Shot%202014-05-26%20at%203.46.23%20PM.png)

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403018680895_Screen%20Shot%202014-05-26%20at%203.46.18%20PM.png)

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_dAp44FpLIZu_p.194591_1403018606615_Screen%20Shot%202014-06-13%20at%204.12.59%20PM.png)

He has the best T-shirts ever

This pad text is synchronized as you type, so that everyone viewing this page sees the same text.  This allows you to collaborate seamlessly on documents!