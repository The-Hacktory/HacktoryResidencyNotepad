# Intro To Processing

1941 University of Pennsylvania

the first computer

to calculate trajectory of ballistics

![](http://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Eniac.jpg/800px-Eniac.jpg)

[p](http://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Eniac.jpg/800px-Eniac.jpg)rogrammed by undergraduate female mathematics students (the men were abroad fighting in WWII)

1962

The very first computer-created artwork by

A. Michael Noll (and co-credited created by the computer)

![](http://www.dam.org/mix/noll-all-artworks-gaussian-quadratic--dam-13320-vK22o-de-2.jpg)

Coordinates in Processing

![](http://www.processing.org/tutorials/drawing/imgs/1.7.jpg)

**Interactivity**

void setup(){

}

void draw(){

}

**A Basic Program**

void setup(){

*   size(400,400);
*   background;

}

void draw(){

}

**Datatypes**

Fixed-point (whole numbers of varying lengths)

Floating-point (decimal numbers of varying lengths)

**Java Datatypes**

Integers values

Floating point

boolean

character

string

**Moving between types**

*   int i = (int) random(1,10);
*       //success!
**   float j = i; //works - why?
*

**Repetitive Tasks**

Let's loop!

*   for(int i=0; i<numTimes; i++){
*       doStuff(i);
*       }

**Our first attempt at making A Michael Noll's composition from 1961**

*   void setup(){
*     size(400,400);
*     background(255);
*   }
**   void draw(){
*     for(int i=0; i<101;i++){
*       int x = 50;
*       int y = 50;
*       int endx = (int)random(0,400);
*       int endy = (int)random(0,400);
*       line(x,y,endx,endy);}
*   }

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_I1SoypTo58e_p.188774_1404862483449_Screen Shot 2014-07-08 at 7.34.22 PM.png)

Slowed-down. Randomly-placed lines.

*   void setup(){
*     size(400,400);
*     background(255);
*     frameRate(10);
*   }
**   void draw(){
*     for(int i=0; i<101;i++){
*       int x = (int)random(0,400);
*       int y = (int)random(0,400);
*       int endx = (int)random(0,400);
*       int endy = (int)random(0,400);
*       line(x,y,endx,endy);
*       
*     }
*   }
*   ![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_I1SoypTo58e_p.188774_1404862615085_Screen Shot 2014-07-08 at 7.36.17 PM.png)
*

**Making Decisions**

AKA conditional statements

Boolean logic ( < > <= >= == !=TRUE/FALSE)

*   if (condition1 == TRUE)
*       doSomething;
*    else if( condition2 == TRUE)
*       doSomethingElse
*    else
*       failsafe;
*       

Updated version of our program

*   void setup(){
*     size(400,400);
*     background(255);
*     frameRate(1);
*   }

*   int endx = (int)random(0,400);
*   int endy = (int)random(0,400);    
*       
*   void draw()
*   {
*     for(int i=0; i<101;i++)
*     {
*       int endx = (int)random(0,400);
*       int endy = (int)random(0,400);
*       int x = endx;
*       int y = endy;
*       float leftOrRight = random(0,1);
*       if(leftOrRight > .5){
*         x = (int)random(0,400);
*       }
*       else
*       {
*         y = (int)random(0,400);
*       }
*       line(x,y,endx,endy);
*       endx = x;
*       endy = y;
*       
*     }
*     noLoop();
*   }
*       

**Random Values**

*   random(high);//between 0-high
*   random(low, high);
*   noise(x,y); //2D Perlin noise
*   randomGaussian();

**Color Representation**

![](http://www.processing.org/tutorials/color/imgs/selector.jpg)

HSB = Hue, Saturation, Brightness

**Color**

*   color c1 = color(r, g, b);
*   color c2 = #RRGGBB;
**   ![](http://www.processing.org/tutorials/color/imgs/rgb.jpg)

**Color + Alpha**

RGBA

-a = alpha / transparency /opacity

-O = transparent; 255 = opaque(solid)

color c1 = color(r, g, b, a);

**Luminance**

aka greyscale

background(255);

![](http://www.processing.org/tutorials/color/imgs/grayscale.jpg)

**Mondrian**

![](http://www2.fiu.edu/~andiaa/cg2/mon_09.jpg)

A Michael Noll's Mondrian

![](http://translab.burundi.sk/code/vzx/1964.MichaelNoll.ComputerCompositionWithLines.jpg)

Composition With Lines

**Session 2**

**Inspiration**

Aleatoric Art

Bringing in random processes into your art

Automatism

![](http://blog.cleveland.com/pdextra/2007/10/large_pollock8.jpg)

**Scope**

Scope is bounded by curly braces.

*   void draw()
*   {
*    for (int i=0; i<width;i++{
*     {
*       ellipse(i*10, i*10,i,i);
*       }
*       rect(width-1, height -i, i, i);
*       //fails because i is outside the for loop
*     }
*       
*      **INSTEAD**
*    void draw()
*    {
*       int i = 0;
*       for( i=0; i<width; i++)
*       {
*         ellipse(i*10, i*10, i, i);
*       }
*       rect(width - i, height - i, i, i); //success!
*     }

George Nees 1970s computer art

![](http://elartedigital.files.wordpress.com/2010/04/schotter-nees.jpg)

Recreate this artwork via code

**Logic**

*   if(mouseX > 200){
*   //do something
*   }
*   else
*   { 
*   //do something else
*   }
*

**Compound Logic**

&&  - AND

||  - OR

!  - NOT

*   if (mouseX>200 && mouseX<400)
*   { 
*   rect (1,1,10,10);
*   //do something
*   }
*

**Arrays**

*   int numEllipses = 10;
*   int paletteLength = 4;
*   color[] palette = new color[paletteLength];
*   palette[0] = #ff00cc;
*   palette[1] = 255;
*   palette[2] = color(255,0,128);
*   palette[3] = color(255,0,64);
**   for(int i=0; i<numEllipses; i++)
*   {
*      color c = palette[(int)random(paletteLength)];
*      fill(c);
*      rect(random(width), random(height), 100, 100);
*   }

A La Recherche De Paul Klee by Vera Molnar

![](http://2.bp.blogspot.com/-ME8r4fB_MpI/ULzna3BklGI/AAAAAAAAAP0/fsQuOA-YAG4/s1600/2+sans+titre+cycle+a+paul+klee)+1969+encre+de+chine+sur+papier+30+x+30+dessin+%C3%A0+l+ordi.jpg)

**Paul Klee homework**

-respect color, form, theme ('characters")

-Make use of rect and lines, loops, random values, arrays

Produce several output images

  