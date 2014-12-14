# CODE

*   **<u>ATAN2 CODE </u>**

import controlP5.*;

ControlP5 cp5;

String url1, url2, url3, url4;

Ground ground;

float x1, y1, x2, y2;

float x, y;

void setup() {

  size(650, 650);

  background(255);

  cp5 = new ControlP5(this);

  cp5.addTextfield("x_1").setPosition(20, height - 380).setSize(60, 20).setAutoClear(false);

  cp5.addTextfield("y_1").setPosition(20, height - 310).setSize(60, 20).setAutoClear(false);

  cp5.addTextfield("x_2").setPosition(20, height - 240).setSize(60, 20).setAutoClear(false);

  cp5.addTextfield("y_2").setPosition(20, height - 170).setSize(60, 20).setAutoClear(false);

  cp5.addBang("Submit").setPosition(20, height - 100).setSize(80, 40);    

 // x1 = 100;

 // y1 = 140;

 // x2 = 400;

 // y2 = 350; 

  //ground = new Ground(x1, y1, x2, y2);

}

void draw() {

  //background(255, 0 );

  //math();

}

void Submit() {

  print("the following text was submitted :");

  url1 = cp5.get(Textfield.class,"x_1").getText();

  x1= float(url1);

  url2 = cp5.get(Textfield.class,"y_1").getText();

  y1 = float(url2);

  url3 = cp5.get(Textfield.class,"x_2").getText();

  x2 = float(url3);

  url4 = cp5.get(Textfield.class,"y_2").getText();

  y2 = float(url4);

  math(x1, y1, x2, y2);

  //new Ground(x1, y1, x2, y2);

  print(" textInput 1 = " + url1);

  print(" textInput 2 = " + url2);

  print(" textInput 3 = " + url3);

  print(" textInput 4 = " + url4);

  println();

  //textSize(16);

  //fill(0, 255, 0, 40);

  //text(url1, 0, -20);

  //text(degrees(ground.rot), 20, 20);

}

class Ground {

  float x1, y1, x2, y2;  

  float x, y, len, rot;

  float ANG;

  PVector X_Y_1;

  PVector X_Y_2;

  //PVector ANG;

  // Constructor

  Ground(float x1, float y1, float x2, float y2) {

    this.x1 = x1;

    this.y1 = y1;

    this.x2 = x2;

    this.y2 = y2;

    x = (x1+x2)/2;

    y = (y1+y2)/2;

    len = dist(x1, y1, x2, y2);

    rot = atan2((y2-y1), (x2-x1));

    X_Y_1 = new PVector (x1, y1);

    X_Y_2 = new PVector (x2, y2);

    ANG = PVector.angleBetween(X_Y_1, X_Y_2);

    println("Angle Between", degrees(rot));

    println(rot);

  }

}

void math(float x1_, float y1_, float x2_, float y2_) { //float x1_, float y1_, float x2_, float y2_

    background(255, 5);

  x1 = x1_;

  y1 = y1_; 

  x2 = x2_; 

  y2 = y2_;

  ground = new Ground(x1, y1, x2, y2);

  //background(255);

  pushMatrix();

  //rectMode(CENTER);

  //translate(width/2, height/2);

  fill(255, 60);

  stroke(0, 255, 0, 100);

  strokeWeight(1);

  line(ground.x1, ground.y1, ground.x2, ground.y2);

  ellipse(ground.x, ground.y, 20, 20);

  strokeWeight(2);

  stroke(200, 255, 0, 100);

  ellipse(ground.x1, ground.y1, 20, 20);

  ellipse(ground.x2, ground.y2, 20, 20);

  popMatrix();

  pushMatrix();

  //rectMode(CENTER);

  translate(ground.x, ground.y);

  textSize(12);

  fill(255, 0, 255);

  text("ground x & y", ground.x, ground.y);

  stroke(255, 0, 255, 40);

  strokeWeight(1);

  line(-400, 0, 400, 0);

  line(0, -400, 0, 400);

  popMatrix();

  pushMatrix();

  translate(ground.x, ground.y);

  rotate(ground.rot);

  textSize(16);

  fill(0, 255, 0, 40);

  text("ground 0 + ROT", 0, -20);

  text(degrees(ground.rot), 20, 20);

  stroke(0, 255, 0, 40);

  strokeWeight(1);

  line(0, 0, 300, 0);

  popMatrix();

  pushMatrix();

  translate(ground.x, ground.y);

  rotate(ground.rot);

  textSize(16);

  fill(0, 255, 0, 40);

  text("ground 0 + ROT", 0, -20);

  text(degrees(ground.rot), 20, 20);

  stroke(255,0, 0, 70);

  strokeWeight(1);

  line(0, 0, 300, 0);

  popMatrix();

  pushMatrix();

  translate(ground.x, ground.y);

  rotate(PI-ground.rot);

  textSize(16);

  fill(0, 255, 0, 40);

  text("ground 0 + ROT", 0, -20);

  text(degrees(ground.rot), 20, 20);

  stroke(255,0, 0, 70);

  strokeWeight(1);

  line(0, 0, 300, 0);

  popMatrix();

}

//line(0, 0, 300, 0);

/* pushMatrix();

 noFill();

 translate(ground.x, ground.y);

 rotate(ground.rot);

 rectMode(CENTER); // works with line as well

 stroke(0, 0, 255, 40);

 strokeWeight(1);

 //line(0, 0, 300, 0);

 popMatrix();

 pushMatrix();

 translate(ground.x, ground.y);

 stroke(0, 0, 255, 40);

 strokeWeight(1);

 line(0, 0, 300, 0);

 popMatrix();

 pushMatrix();

 rectMode(CENTER);

 translate(ground.x, ground.y);

 textSize(12);

 fill(255, 0, 255);

 text("ground x & y", ground.x, ground.y);

 stroke(255, 0, 255, 40);

 strokeWeight(1);

 line(-400, 0, 400, 0);

 line(0, -400, 0, 400);

 popMatrix();

 pushMatrix();

 translate(ground.x, ground.y);

 rotate(ground.rot);

 textSize(16);

 fill(0, 255, 0, 40);

 text("ground 0 + ROT", 0, -20);

 text(degrees(ground.rot), 20, 20);

 stroke(0, 255, 0, 40);

 strokeWeight(1);

 line(0, 0, 300, 0);

 popMatrix();

 */