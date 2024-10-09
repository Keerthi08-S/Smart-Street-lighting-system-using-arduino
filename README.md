# Smart-Street-lighting-system-using-arduino
int motionPin = 2;
int lightPin = 9;
int sensorVal = 0;

void setup() 
{
  pinMode(motionPin, INPUT);
  pinMode(lightPin, OUTPUT);
}
void loop() 
{
  sensorVal = digitalRead(motionPin);
  if (sensorVal == HIGH) 
  {
    analogWrite(lightPin, 255); 
  } 
  else 
  {
    analogWrite(lightPin, 100);
  }
  delay(1000);
}
