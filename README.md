# game
float a;
float b;
float dx = 1;
float dy = 1;
 
float accx = 0.5;
float accy = 0.8;
float xb;
float yb;
 
float x;
float y;
 
float pct = 0.05;
int e = 400;
int r =400;
int rad=100;
boolean isClicked=false ;
void setup() {
 
  size(800, 800);
}
void draw() {
 
  background(0);
  if (isClicked==false) {
    fill(#F0C4ED);
        rect (e-50, r-50, rad, rad);
  fill(#A249E3);
  text("Start",367,407);
  textSize(30);
  } else {
   xb = mouseX;
  yb = mouseY;
 
  x = x + (xb-x)*pct;
  y = y + (yb-y)*pct;
 
  if(isClicked=true){
      background(255);
pushMatrix();
translate(x-240,y-240);
  background(#E349DB);
 
   background(#95DDF2);
  
  
  
  //draxing head
  noStroke();
  fill(#FCFC08);
  rect(100,100,200,225);
  
  fill(#ffffff);
  ellipse(160,150,50,50);

  fill(#ffffff);
  ellipse(240,150,50,50);
  
  
  fill(#08C9FC);
  ellipse(230,150,20,20);
  
  fill(#08C9FC);
  ellipse(170,150,20,20);
  
  fill(#000000);
  ellipse(225,150,10,10);
  
  fill(#000000);
  ellipse(174,150,10,10);
  
  //pants
  
  fill(#ffffff);
  quad(100,325,300,325,290,355,110,355);
  
  fill(#76551E);
  quad(290,355,110,355,120,375,280,375);
  
  fill(#030000);
  rect(245,365,25,5);
  
  fill(#030000);
  rect(205,365,25,5);
  
  fill(#030000);
  rect(165,365,25,5);
  
  
  fill(#030000);
  rect(125,365,25,5);
  
  fill(#ffffff);
  rect(150,375,8,70);
  
  //legs
  fill(#FCFC08);
  rect(150,375,8,70);
  
  fill(#FCFC08);
  rect(240,375,8,70);
  
  fill(#ffffff);
  rect(150,420,8,50);
  
  fill(#ffffff);
  rect(240,420,8,50);
  
  fill(#030000);
  ellipse(154,470,10,20);
  
  fill(#030000);
  ellipse(244,470,10,20);
  
  //background circles
  
  fill(#95DDF2);
  ellipse(97,96,30,30);
  
  fill(#95DDF2);
  ellipse(97,156,30,30);
  
  fill(#95DDF2);
  ellipse(97,236,40,30);
  
  fill(#95DDF2);
  ellipse(97,286,20,30);
  
  fill(#95DDF2);
  ellipse(177,106,20,20);
  
  
  fill(#95DDF2);
  ellipse(237,106,10,20);
  
  fill(#95DDF2);
  ellipse(297,146,10,20);
  
  fill(#95DDF2);
  ellipse(297,196,20,20);
  
   fill(#95DDF2);
  ellipse(297,256,30,30);
  
  
  fill(#95DDF2);
  ellipse(297,296,20,20);
  
 //mouth
 
 
 
 
 fill(#030000);
 ellipse(200,280,120,70);
  
  fill(#FCFC08);
 ellipse(200,260,100,70);
  
  //arms
  
  fill(#FCFC08);
  rect(80,210,40,10);
  
  fill(#FCFC08);
  rect(280,210,40,10);
  
  
   fill(#FCFC08);
  rect(70,210,10,90);
  
  fill(#FCFC08);
  rect(320,210,10,90);
  
  
  
}
  popMatrix();
  }
 
 
  a = a+accx*dx;
  b = b +accy*dy;
 
  if (a > width || a < 0)
  {
    accx = random(0.1,5);
    dx = dx*-1;
  }
 
  if ( b> height || b < 0) {
    accy = random(0.1,5);
    dy = dy*-1;
  }
 
 
  fill(0);
  noStroke();
  ellipse(a, b, 30, 30);
}
  
 
 
 
 
 
void mouseClicked() {
  float d = dist(mouseX, mouseY, e, r);
  if ( d<rad/2 ) {
    isClicked=true;
  } else {
    isClicked=false;
  }
}
 
