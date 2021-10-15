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
void setup() <br>
{ <br>
  pinMode(8, OUTPUT);<br>
}<br> 
void loop() <br>
{<br>
  digitalWrite(8, HIGH);<br>
  delay(1000);<br>
  digitalWrite(8, LOW);<br>
  delay(1000);<br>
}<br>


### Video
<iframe Width="600" height="315" src="http://" title=" Youtube video player>
                                                     
                                                      
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
                                                      
int redled =10; // initialize digital pin 8.<br>
int yellowled =7; // initialize digital pin 7.<br>
int greenled =4; // initialize digital pin 4.<br>
void setup()<br>
{<br>
pinMode(redled, OUTPUT);// set the pin with red LED as “output”<br>
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”<br>
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”<br>
}<br>
void loop()<br>
{<br>
digitalWrite(greenled, HIGH);//// turn on green LED<br>
delay(5000);// wait 5 seconds<br>

digitalWrite(greenled, LOW); // turn off green LED<br>
for(int i=0;i<3;i++)// blinks for 3 times<br>
{<br>
delay(500);// wait 0.5 second<br>
digitalWrite(yellowled, HIGH);// turn on yellow LED<br>
delay(500);// wait 0.5 second<br>
digitalWrite(yellowled, LOW);// turn off yellow LED<br>
} <br>
delay(500);// wait 0.5 second<br>
digitalWrite(redled, HIGH);// turn on red LED<br>
delay(5000);// wait 5 seconds<br>
digitalWrite(redled, LOW);// turn off red LED<br>
}<br>
 
### Video
<iframe Width="600" height="315" src="http://" title=" Youtube video player>
 
  
## Experiment 3 : LED Chasing Effect

### Hardware required
*Led x6
*Arduino board x1
*220Ω resistor x6
*Breadboard x1
*USB cable x1
*Breadboard wire x13                                                    

### Code
  int BASE = 2 ;  // the I/O pin for the first LED<br>
int NUM = 6;   // number of LEDs<br>
void setup()<br>
{<br>
   for (int i = BASE; i < BASE + NUM; i ++) <br>
   {<br>
     pinMode(i, OUTPUT);   // set I/O pins as output<br>
   }<br>
}<br>
void loop()<br>
{<br>
   for (int i = BASE; i < BASE + NUM; i ++) <br>
   {<br>
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.<br>
     delay(200);        // delay<br>
   }<br>
   for (int i = BASE; i < BASE + NUM; i ++) <br>
   {<br>
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one<br>
     delay(200);        // delay<br>
   }  <br>
}<br>
                            
                              
### Video
<iframe Width="600" height="315" src="http://" title=" Youtube video player>
 
  
  
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
  int ledpin=11;// initialize pin 11<br>
int inpin=7;// initialize pin 7<br>
int val;// define val<br>
void setup()<br>
{<br>
pinMode(ledpin,OUTPUT);// set LED pin as “output”<br>
pinMode(inpin,INPUT);// set button pin as “input”<br>
}<br>
void loop()<br>
{<br>
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val<br>
if(val==LOW)// check if the button is pressed, if yes, turn on the LED<br>
{ digitalWrite(ledpin,LOW);}<br>
else<br>
{ digitalWrite(ledpin,HIGH);}<br>
}<br>
  
### Video
<iframe Width="600" height="315" src="http://" title=" Youtube video player>

                                                      
                                                      
## Experiment 5 :  Buzzer
                                                      
### Hardware Required
*Arduino Uno
*Buzzer x1
*Breadboard x1
*Breadboard Jumper Wire x2
*USB cable x1                                                      
  
### Code
int buzzer=8;// initialize digital IO pin that controls the buzzer<br>
void setup() <br>
{ <br>
  pinMode(buzzer,OUTPUT);// set pin mode as “output”<br>
} <br>
void loop() <br>
{<br>
digitalWrite(buzzer, HIGH); // produce sound<br>
}<br>
                                                      
### Video
<iframe Width="600" height="315" src="http://" title=" Youtube video player>                                                      
