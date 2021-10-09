# Kerala IoT challenge
## About Me
>**Hey folks!** I'm **Muhammed Hisham**. I'm currently pursuing my Bachelor's degree(4th year)  in Electrical and Electronic Engineering at **College Of Engineering Trikaripur,Kasargod**.
This page is created to exibit my activities and experiments on IoT.
## Experiment 1 -Hello World LED Blinking

### Hardware needed
* Arduino Uno Board x1
* USB Cable xl
* LED (Any Color)x1
* 220 OHM Resistor x1
* Breadboard
* Jumber Wires (male to male) x2

### code

int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}


### Video
<iframe Width="600" height="315" src="http://" title=" Youtube video player>
__                                                      
                                                      
## Experiment 2 : Traffic Light
                                                      
###  Hardware needed
* Arduino Uno Board x1
* USB Cable xl
* RED  M5 LED x1
* YELLOW M5 LED x1
* GREEN M5LED x1                                                     
* 220 OHM Resistor x1
* Breadboard
* Breadboard Jumber Wires are needed

### Code
int redled =10; // initialize digital pin 8.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds

digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}
 
### Video
<iframe Width="600" height="315" src="http://" title=" Youtube video player>
___  
  
## Experiment 3 : LED Chasing Effect

### Hardware required
*Led x6
*Arduino board x1
*220Ω resistor x6
*Breadboard x1
*USB cable x1
*Breadboard wire x13                                                    

### Code
  int BASE = 2 ;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(200);        // delay
   }  
}
                              
                              
### Video
<iframe Width="600" height="315" src="http://" title=" Youtube video player>
 ___ 
 ## Experiment 4 : Button Controlled LED
  
 ### Hardware Required
*Arduino Uno
*Button switch x1
*Red M5 LED x1
*220ΩResistor x1
*10KΩ Resistor x1
*Breadboard x1
*Breadboard Jumper Wire x6
*USB cable x1
  
 ### Code
  int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}
  
### Video
<iframe Width="600" height="315" src="http://" title=" Youtube video player>
___                                                      
## Experiment 5 :  Buzzer
                                                      
### Hardware Required
*Arduino Uno
*Buzzer x1
*Breadboard x1
*Breadboard Jumper Wire x2
*USB cable x1                                                      
  
 ### Code
int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}
                                                      
### Video
<iframe Width="600" height="315" src="http://" title=" Youtube video player>                                                      
