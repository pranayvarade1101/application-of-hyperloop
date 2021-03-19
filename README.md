# application-of-hyperloop
Working on small scale application of hyperloop in hospitals for immediate 
supply of medication

 Receiver_ arduino_with_motor.c

#define datain A0
#define ledPin 12
unsigned int temp = 0;
const unsigned int upperThreshold = 600;
const unsigned int lowerThreshold = 50;
void setup()
{
    pinMode(ledPin, OUTPUT);
}
void loop()
{
    temp=analogRead(datain);
    if(temp<lowerThreshold)
    {
        digitalWrite(ledPin, HIGH);
    }
    else if
    (temp>upperThreshold)
    {
        digitalWrite(ledPin, LOW);
    }
}





✓ Transmitter_arduino_with_IRsensor

#define dataout 12
#define ledPin 7
void setup()
{
    pinMode(dataout, OUTPUT);
    pinMode(ledPin, OUTPUT);
}
void loop()
{
    digitalWrite(dataout, HIGH);
    digitalWrite(ledPin, HIGH);
    delay(200);
    digitalWrite(dataout,LOW);
    digitalWrite(ledPin, LOW);
    delay(200);
}



✓IR sensor_to_Arduino

void setup()
{
    pinMode(13,OUTPUT);
    pinMode(3,INPUT);
    Serial.begin(9600);
}
void loop()
{
    if (digitalRead(3)== LOW)
    {
        digitalWrite(13,HIGH);
        delay(10);
    }
    else
    {
        digitalWrite(13,LOW);
        delay(10);
    }
}

