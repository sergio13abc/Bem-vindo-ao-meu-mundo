# Bem-vindo-ao-meu-mundo
/*
El control de la posicion de un servo usando un potenciometro (resistor variable)
by Sergio, Yenny, Michell, Marco
*/

#include <Servo.h>

Servo servo1; 
Servo servo2;// create servo object to control a servo

void setup() {
  servo1.attach(10); 
  servo2.attach(9);// attaches the servo on pin 9 to the servo object

  //leds1

  pinMode(13, OUTPUT);  pinMode(12, OUTPUT); pinMode(11, OUTPUT);

  //leds2

  pinMode(7, OUTPUT);  pinMode(6, OUTPUT); pinMode(5, OUTPUT);
  
}

void loop() {
   /* 
  digitalWrite(13, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);              // wait for a second
  digitalWrite(13, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);*/
  
  servo1.write(180);                  // sets the servo position according to the scaled value
  delay(150);   
  /*
  digitalWrite(12, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);              // wait for a second
  digitalWrite(12, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);*/
  servo2.write(60);                  // sets the servo position according to the scaled value
  delay(150);  // waits for the servo to get there

   
  servo1.write(80);                  // sets the servo position according to the scaled value
  delay(150);   
  /*
  digitalWrite(12, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);              // wait for a second
  digitalWrite(12, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);*/
  servo2.write(80);                  // sets the servo position according to the scaled value
  delay(150);  // waits for the servo to get there
}
