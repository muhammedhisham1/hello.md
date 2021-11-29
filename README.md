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
<video src="https://user-images.githubusercontent.com/84323483/143879324-fdc6935f-1729-4fa8-857f-8e5323b4fd4a.mp4"></video>

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
<video src="https://user-images.githubusercontent.com/84323483/143879544-ae639c96-2662-4e69-a4df-325742a18758.mp4"></video>


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
<image src="![lm35](https://user-images.githubusercontent.com/84323483/143880499-579e1ff1-54d6-4553-9399-cfcc25b0febf.png)" controls="" width="50%" height="150%"></image>



### Experiment image
 <image src="![photo_2021-11-29_19-27-40](https://user-images.githubusercontent.com/84323483/143880943-418e030c-d717-46c7-8995-d4de7029b6a9.jpg)" controls="" width="50%" height="150%"></image>                                       

                                              
