# Smart-Fire-Detection
Smart Fire Detection uses advanced sensors and AI to quickly and accurately detect fires, reducing false alarms. These systems provide real-time alerts and automate safety measures like activating sprinklers and unlocking exits. Integrated with smart home devices, they enhance fire response efficiency.



Code:
// Define pins for ultrasonic and buzzer Code- Fire Alarm System Using Arduino
const int ledpin=13;
const int flamepin=A2;
const int buzpin=11;
const int threshold=200;// sets threshold value for flame sensor
int flamesensvalue=0; // initialize flamesensor reading
void setup()
Serial.begin(9600);
pinMode(ledpin,OUTPUT);
pinMode(flamepin,INPUT);
pinMode(buzpin,OUTPUT);
void loop()
flamesensvalue=analogRead(flamepin); // reads analog data from flame sensor
if (flamesensvalue¡=threshold) // compares reading from flame sensor with the threshold
digitalWrite(ledpin,HIGH); //turns on led and buzzer
tone(buzpin,100);
delay(1000); //stops program for 1 second
else
digitalWrite(ledpin,LOW); //turns led off led and buzzer
noTone(buzpin);
