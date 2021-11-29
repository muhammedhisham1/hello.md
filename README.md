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

### video
<video src="https://user-images.githubusercontent.com/84323483/139533478-c72c3b34-ae53-41a2-9a2a-47894863fa30.mp4" controls="" width="50%" height="150%"></video>

                                                      
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
### video
<video src="https://user-images.githubusercontent.com/84323483/139533812-d6b19522-c7ad-475d-a2e4-48a28e977081.mp4" controls="" width="50%" height="150%"></video>

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
                              
### video
<video src="https://user-images.githubusercontent.com/84323483/139533852-394b1d95-5546-4ff4-a7e0-c5cf8d3a5c28.mp4" controls="" width="50%" height="150%"></video>


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
### video

<video src="https://user-images.githubusercontent.com/84323483/139533956-993eb639-5db0-446d-817b-ddd67897f1b9.mp4" controls="" width="50%" height="150%"></video>
                                                                      
                                                      
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
### video
<video src="https://user-images.githubusercontent.com/84323483/139534143-ca70023c-3e5a-4495-a4d3-5a0676265715.mp4" controls="" width="50%" height="150%"></video>
                                                   
                                                   
## Experiment 6:  RGB LED
                                                      
### Hardware Required
* Arduino Uno
* RGB Led x1
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

                    
                                                   
## Experiment 7:  LDR Light Sensor
                                                      
### Hardware Required
* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1
                                                   
  
### Code
```                                                      
int potpin=0;// initialize analog pin 0, connected with photovaristor
int ledpin=11;// initialize digital pin 11, 
int val=0;// initialize variable val
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin 11 as “output”
Serial.begin(9600);// set baud rate at “9600”
}
void loop()
{
val=analogRead(potpin);// read the value of the sensor and assign it to val
Serial.println(val);// display the value of val
analogWrite(ledpin,val/4);// set up brightness（maximum value 255）
delay(10);// wait for 0.01 
}
 ```                                                     
### video 
<video src="https://user-images.githubusercontent.com/84323483/143883518-6ee0c9b4-edb7-4576-86cf-ddf8ad824f42.mp4" controls="" width="50%" height="150%"></video>
## Experiment 8: Flame Sensor
                                                      
### Hardware Required
* Arduino Uno Board*1
* Flame Sensor *1
* Buzzer *1
* 10K Resistor *1
* Breadboard Jumper Wire*6
* USB cable*1                                                    
  
### Code
``` 
int flame=0;// select analog pin 0 for the sensor
int Beep=9;// select digital pin 9 for the buzzer
int val=0;// initialize variable
 void setup() 
{
  pinMode(Beep,OUTPUT);// set LED pin as “output”
 pinMode(flame,INPUT);// set buzzer pin as “input”
 Serial.begin(9600);// set baud rate at “9600”
 } 
void loop() 
{ 
  val=analogRead(flame);// read the analog value of the sensor 
  Serial.println(val);// output and display the analog value
  if(val>=600)// when the analog value is larger than 600, the buzzer will buzz
  {  
   digitalWrite(Beep,HIGH); 
   }else 
   {  
     digitalWrite(Beep,LOW); 
    }
   delay(500); 
}

 ```                                                     
### video
<video src="https://user-images.githubusercontent.com/84323483/143879544-ae639c96-2662-4e69-a4df-325742a18758.mp4" controls="" width="50%" height="150%"></video>


## Experiment 9 :  LM35 Temperature Sensor
                                                      
### Hardware Required
* Arduino Uno  Board*1
* LM35*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*                                                      
  
### Code
```                                                      
int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(0);// read the analog value of the sensor and assign it to val
dat=(125*val)>>8;// temperature calculation formula
Serial.print("Tep");// output and display characters beginning with Tep
Serial.print(dat);// output and display value of dat
Serial.println("C");// display “C” characters
delay(500);// wait for 0.5 second
}
 ```
### Serial Monitor Output 
![lm35](https://user-images.githubusercontent.com/84323483/143880499-579e1ff1-54d6-4553-9399-cfcc25b0febf.png)"

### Experiment image
                                    
![photo_2021-11-29_19-36-41](https://user-images.githubusercontent.com/84323483/143882302-6bd936bb-5e15-44dc-b3e5-a7a36fd1d637.jpg)

## Experiment 10: IR Remote Control Using TSOP
                                                      
### Hardware Required
* Arduino Uno Board*1
* Infrared Remote Controller(You can use TV Remote or any other remote) *1
* Infrared Receiver *1
* LED *6
* 220ΩResistor *6
* Breadboard Wire *11
* USB cable*1                                                 
  
### Code
``` 
#include <IRremote.h>
int RECV_PIN = 11;
int LED1 = 2;
int LED2 = 3;
int LED3 = 4;
int LED4 = 5;
int LED5 = 6;
int LED6 = 7;
long on1  = 0x0080412701;
long off1 = 0x0080412702;
long on2 = 0x0080412702;
long off2 = 0x0080412703;
long on3 = 0x0080412703;
long off3 = 0x0080412704;
long on4 = 0x0080412704;
long off4 = 0x0080412705;
long on5 = 0x0080412705;
long off5 = 0x0080412706;
long on6 = 0x0080412706;
long off6 = 0x0080412707 ;
IRrecv irrecv(RECV_PIN);
decode_results results;
void setup()
 {
  pinMode(RECV_PIN, INPUT);   
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
  pinMode(LED3, OUTPUT);
  pinMode(LED4, OUTPUT);
  pinMode(LED5, OUTPUT);
  pinMode(LED6, OUTPUT);  
  pinMode(13, OUTPUT);
  Serial.begin(9600);
   irrecv.enableIRIn(); // Start the receiver
 }
int on = 0;
unsigned long last = millis();
void loop() 
{
  if (irrecv.decode(&results)) 
   {
    // If it's been at least 1/4 second since the last
    // IR received, toggle the relay
    if (millis() - last > 250) 
      {
       on = !on;
//       digitalWrite(8, on ? HIGH : LOW);
       digitalWrite(13, on ? HIGH : LOW);
      
      }
    if (results.value == on1 )
       digitalWrite(LED1, HIGH);
    if (results.value == off1 )
       digitalWrite(LED1, LOW); 
    if (results.value == on2 )
       digitalWrite(LED2, HIGH);
    if (results.value == off2 )
       digitalWrite(LED2, LOW); 
    if (results.value == on3 )
       digitalWrite(LED3, HIGH);
    if (results.value == off3 )
       digitalWrite(LED3, LOW);
    if (results.value == on4 )
       digitalWrite(LED4, HIGH);
    if (results.value == off4 )
       digitalWrite(LED4, LOW); 
    if (results.value == on5 )
       digitalWrite(LED5, HIGH);
    if (results.value == off5 )
       digitalWrite(LED5, LOW); 
    if (results.value == on6 )
       digitalWrite(LED6, HIGH);
    if (results.value == off6 )
       digitalWrite(LED6, LOW);        
    last = millis();      
irrecv.resume(); // Receive the next value
  }
}

 ```                                                     
### video
<video src="https://user-images.githubusercontent.com/84323483/143882998-4a2e3aaf-2d2e-4a62-8e4f-6195c5cc0723.mp4" controls="" width="50%" height="150%"></video>

## Experiment 11 :  Potentiometer analog Value Reading
                                                      
### Hardware Required
* Arduino Uno Board*1]
* 10K Potentiometer *1
* Breadboard*1
* Breadboard Jumper Wire*3
* USB cable*1                                                    
  
### Code
```                                                      
int potpin=0;// initialize analog pin 0
int ledpin=13;// initialize digital pin 13
int val=0;// define val, assign initial value 0
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin as “output”
Serial.begin(9600);// set baud rate at 9600
}
void loop()
{
digitalWrite(ledpin,HIGH);// turn on the LED on pin 13
delay(50);// wait for 0.05 second
digitalWrite(ledpin,LOW);// turn off the LED on pin 13
delay(50);// wait for 0.05 second
val=analogRead(potpin);// read the analog value of analog pin 0, and assign it to val 
Serial.println(val);// display val’s value
}
 ```
### Serial Monitor Output 
![potentiometre](https://user-images.githubusercontent.com/84323483/143884286-d078ad90-1a49-480d-843b-1ecb1c37e875.png)

### Experiment
![photo_2021-11-29_19-53-49](https://user-images.githubusercontent.com/84323483/143885038-54f57e38-477e-4c5d-a987-bcc984b786a8.jpg)
 image
                                             
## Experiment 12:  7 Segment Display
                                                      
### Hardware Required
* Arduino Uno Board*1
* 1-digit LED Segment Display*1
* 220Ω Resistor*8
* Breadboard*1
* Breadboard Jumper Wires *several
* USB cable*1
                                                   
  
### Code
```                                                      
int a=7;// set digital pin 7 for segment a
int b=6;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=10;// set digital pin 10 for segment d
int e=11;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp
void digital_0(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
for(j=5;j<=7;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
for(j=8;j<=11;j++)
digitalWrite(j,LOW);
}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=5;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
while(1)
{
digital_0();// display number 0
delay(1000);// wait for 1s
digital_1();// display number 1
delay(1000);// wait for 1s
digital_2();// display number 2
delay(1000); // wait for 1s
digital_3();// display number 3
delay(1000); // wait for 1s
digital_4();// display number 4
delay(1000); // wait for 1s
digital_5();// display number 5
delay(1000); // wait for 1s
digital_6();// display number 6
delay(1000); // wait for 1s
digital_7();// display number 7
delay(1000); // wait for 1s
digital_8();// display number 8
delay(1000); // wait for 1s
digital_9();// display number 9
delay(1000); // wait for 1s
}}
 ```                                                     
### video 
<video src="https://user-images.githubusercontent.com/84323483/143885627-a821c745-eb6a-4b77-a252-4ea5038261c5.mp4" controls="" width="50%" height="150%"></video>

## Assignment 1: Thermometer Using 6 LED s and LM35 Sensor
                                                      
### Hardware Required
* Arduino Uno/Genuino
* Breadboard
* Jumper wires (generic)
* 3 220Ω resistors
* 3 LEDs (any color)
* LM35
### Code
``` 
const int hot = 87; //set hot parameter
const int cold = 75; //set cold parameter
void setup() {
pinMode(A2, INPUT); //sensor
pinMode(2, OUTPUT); //blue
pinMode(3, OUTPUT); //green
pinMode(4, OUTPUT); //red
Serial.begin(9600);
}
void loop() {
int sensor = analogRead(A2);
float voltage = (sensor / 1024.0) * 5.0;
float tempC = (voltage - .5) * 100;
float tempF = (tempC * 1.8) + 32;
Serial.print("temp: ");
Serial.print(tempF);
if (tempF < cold) { //cold
digitalWrite(2, HIGH);
digitalWrite(3, LOW);
digitalWrite(4, LOW);
Serial.println(" It's Cold.");
}
else if (tempF >= hot) { //hot
digitalWrite(2, LOW);
digitalWrite(3, LOW);
digitalWrite(4, HIGH);
Serial.println(" It's Hot.");
}
else { //fine
digitalWrite(2, LOW);
digitalWrite(3, HIGH);
digitalWrite(4, LOW);
Serial.println(" It's Fine.");
}
delay(10);
}

 ```                                                     
### video
<video src="https://user-images.githubusercontent.com/84323483/143887763-ef0aaa96-9828-4fd8-b719-506e3d399fa7.mp4" controls="" width="50%" height="150%"></video>


## Assignment 2: Digital Dice Using 7 Segment Display
                                                      
### Hardware Required
* Arduino UNO
* 7 Segment Display
* Push Button
* 7 x 220Ω Resistors (1/4 Watt)
* Breadboard
* Connecting Wires
### Code
``` 
//e = 2;
 //d = 3;
 //c = 4;
 //g = 5;
 //f = 6;
 //a = 7;
 //b = 8;
                 
int num[10][7]={ {0,0,0,1,0,0,0},
                 {1,1,0,1,1,1,0},
                 {0,0,1,0,1,0,0},
                 {1,0,0,0,1,0,0},
                 {1,1,0,0,0,1,0},
                 {1,0,0,0,0,0,1},
                 {0,0,0,0,0,1,1},
                 {1,1,0,1,1,0,0},
                 {0,0,0,0,0,0,0},
                 {1,0,0,0,0,0,0} 
	        };

long r_num;     
int roll = 12;            
bool state = true; 

void setup() 
{
pinMode(2,OUTPUT);
pinMode(3,OUTPUT);
pinMode(4,OUTPUT);
pinMode(5,OUTPUT);
pinMode(6,OUTPUT);
pinMode(7,OUTPUT);
pinMode(8,OUTPUT);
pinMode(9,OUTPUT);
pinMode(12,INPUT_PULLUP);

digitalWrite(2,HIGH);
digitalWrite(3,HIGH);
digitalWrite(4,HIGH);
digitalWrite(5,HIGH);
digitalWrite(6,HIGH);
digitalWrite(7,HIGH);
digitalWrite(8,HIGH);

digitalWrite(9,HIGH);

randomSeed(analogRead(0));

}

void loop() 
{
 if(state)
 {
   r_num=random(1,6);
   for(int i=0;i<7;i++)
    {
      digitalWrite(i+2,num[r_num][i]);
    }
     //delay(1500);
    state=false;
 }

while(digitalRead(roll)==LOW)
{
   for(int i=0;i<10;i++)
    {
     for(int j=0;j<7;j++)
       {
         digitalWrite(j+2,num[i][j]);
       }
     delay(50);
    }
 state=true;
}
}

 ```                                                     
### video
<video src="https://user-images.githubusercontent.com/84323483/143888739-f7664e1d-1c89-4ea0-bd32-8d6568eac717.mp4" controls="" width="50%" height="150%"></video>













