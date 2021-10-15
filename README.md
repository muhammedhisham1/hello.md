# Kerala IoT challenge
## About Me
>**Hey folks!** I'm **Muhammed Hisham**. I'm currently pursuing my Bachelor's degree(4th year)  in Electrical and Electronic Engineering at **College Of Engineering Trikaripur,Kasargod**.
This page is created to exibit my activities and experiments on IoT.


### Experiment 1 -Hello World LED Blinking

### Hardware needed
* Arduino Uno Board x1
* USB Cable xl
* LED (Any Color)x1
* 220 OHM Resistor x1
* Breadboard
* Jumber Wires (male to male) x2

### code
```
void setup()
{ 
  pinMode(8, OUTPUT);
}<br> 
void loop() 
{
  digitalWrite(8, HIGH);
  delay(1000);
  digitalWrite(8, LOW);
  delay(1000);
}
```

### simulation
![Start Simulating](https://user-images.githubusercontent.com/84323483/137472027-0d75b922-a10f-40c4-bdfa-54ee23c10558.png)
                                                      
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
```                                                      
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
 ```
### Simulation
![Start Simulating (1)](https://user-images.githubusercontent.com/84323483/137469168-83254954-6740-4d58-a721-562f17ad528b.png)

 
  
## Experiment 3 : LED Chasing Effect

### Hardware required
* Arduino Uno Board x1
* USB Cable xl
* LED (Any Color)x1
* 220 OHM Resistor x1
* Breadboard
* Jumber Wires (male to male) x2                                                 

### Code
```                                                      
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
   {<br>
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(200);        // delay
   }  
}
 ```                          
                              
### Simulation
![Start Simulating (2)](https://user-images.githubusercontent.com/84323483/137469264-4e8591d4-6d59-4ec7-b364-5272f3b18a33.png)

## Experiment 3 : LED Chasing Effect
 ## Experiment 4 :  Button Controlled LED                                                     
### Hardware Required
* Arduino Uno
* Button switch x1
* Red M5 LED x1
* 220ΩResistor x1
* 10KΩ Resistor x1
* Breadboard x1
* Breadboard Jumper Wire x6
* USB cable x1                                                      
  
### Code
```                                                      
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
```
### Simulation
![Start Simulating (4)](https://user-images.githubusercontent.com/84323483/137473867-dcf15083-d846-48c5-9d64-c50e775e06ee.png)

                           

                                                      
                                                      
## Experiment 5 :  Buzzer
                                                      
### Hardware Required
* Arduino Uno
* Buzzer x1
* Breadboard x1
* Breadboard Jumper Wire x2
* USB cable x1                                                      
  
### Code
```                                                      
int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}
 ```                                                     
### Simulation
![Start Simulating (7)](https://user-images.githubusercontent.com/84323483/137471268-1b407483-0ea9-4f1c-9f35-2e8bcd91e3cf.png)
                                                   
                                                   
## Experiment 6: 
                                                      
### Hardware Required
* Arduino Uno
* RED Led x1
* Resistor x3
* Breadboard x1
* Breadboard Jumper Wire x5
* USB cable x1                                                      
  
### Code
```                                                      
int red = 11;
int blue =10;
int green =9;
int x;
void setup() {
  pinMode(red, OUTPUT);
  pinMode(blue, OUTPUT);
  pinMode(green, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(x=255; x>0; x--)
  {
   analogWrite(11, x);
   analogWrite(10, 255-x);
   analogWrite(9, 128-x);
   delay(10); 
  }
for(x=0; x<255; x++)
  {
   analogWrite(11, x);
   analogWrite(10, 255-x);
   analogWrite(9, 128-x);
   delay(10); 
  }
 Serial.println(x, DEC);
}
 ```                                                     
### Simulation
![Start Simulating (11)](https://user-images.githubusercontent.com/84323483/137471879-8316a53c-ee13-4d44-82db-a877311143fc.png)

                                              
