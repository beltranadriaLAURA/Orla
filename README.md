# import processing.pdf.*;

float rx, rx1, rx2, rx3;
float ry, ry1, ry2, ry3;
boolean record;
PImage img;

void setup() {
  img=loadImage("titulo.png");
 frameRate(6);
  size(800,800);
  }
void draw () {
 background(255);
  
if(record==true){
    beginRecord(PDF,"02processing-###.pdf");
  }
 scale(0.2);
image(img,1200,80);

scale(4);
  rx=random(0,50);
  rx1=random(50,100);
  rx2=random(100,150);
  rx3=random(150,200);
  
  //retratos
  maite(rx1,230);
  miguel(rx,400);
  lauraf(rx3,150);
  eva(550,rx);
  sandra(400,rx1);
  miquel(480,rx2);
  abel(rx3,250);
  diamar(rx2,320);
  nico(100,rx3);
  sergio(280,rx);
  mariag(rx,300);
  laurab(470,rx3);
  scale(0.3);
  aranza(1800,rx);
 if (record==true){
  endRecord();
  record=false;
  }
}
void aranza (float posx, float posy){
pushMatrix();
scale(0.8);
translate (posx, posy);

//pelo
  strokeWeight(6);
  stroke(139, 69, 19);
  line(550, 100, 150, 100);
  line(150, 100, 100, 150);
  line(550, 100, 600, 150);
  line(100, 150, 100, 690);
  line(100, 700, 200, 700);
  line(200, 700, 200, 400);
  line(200, 400, 500, 200);
  line(500, 200, 500, 700);
  line(500, 700, 600, 700);
  line(600, 700, 600, 150);

  //pendientes
  strokeWeight(6);
  stroke(200, 200, 200);
  fill(254, 254, 254);
  ellipse(200, 440, 30, 30);
  ellipse(500, 440, 30, 30);

  //nariz
  stroke(255, 203, 208);
  triangle(340, 420, 360, 410, 330, 410);

  //ojos
  stroke(12, 183, 242);
  fill(255, 255, 255);
  ellipse(310, 340, 60, 60);
  ellipse(390, 340, 60, 60);
  strokeWeight(40);
  stroke(0, 66, 89);
  point(310, 340);
  point(390, 340);
  strokeWeight(20);
  stroke(12, 183, 242);
  point(310, 340);
  point(390, 340);
  stroke(224, 255, 255);
  point(317, 323);
  point(397, 323);

  //gafas
  strokeWeight(4);
  stroke(12, 3, 2);
  noFill();
  ellipse(290, 335, 100, 100);
  ellipse(410, 335, 100, 100);
  line(360, 340, 340, 340);

  //boca
  stroke(250, 20, 100);
  strokeWeight(15);
  line(250, 480, 250, 500);
  line(250, 500, 450, 500);
  line(450, 480, 450, 500);

  //pestañas
  strokeWeight(2);
  stroke(0, 20, 2);
  line(310, 310, 310, 300);
  line(295, 310, 295, 300);
  line(302, 310, 302, 300);
  line(395, 310, 395, 300);
  line(380, 310, 380, 300);
  line(387, 310, 387, 300);
  
popMatrix();
}
void mousePressed(){
    record=true;
  }
