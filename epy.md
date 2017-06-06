PImage img;

void setup() {
  size(1680, 1050); 
  background(0);
  frameRate(42);
  noCursor();
}

void draw() {
   strokeWeight(25);  
   rect(0,0,1680,1050);
   fill(random(255), random(255), random(255));
}

void keyPressed(){
  if(key==27)
    key=0;
}
