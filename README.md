# TRAFFIC-LIGHT-BY-ARDUINO-UNO
int pin2= 2;int pin4= 4;int pin7=7;
int switch_pin = 12;

void setup()
{
  pinMode(pin2, OUTPUT);
  pinMode(pin4, OUTPUT);
  pinMode(pin7, OUTPUT);
  pinMode(switch_pin,INPUT_PULLUP);
}
void loop()
{
  if(digitalRead(switch_pin) == HIGH)//start when switch is on
  {
    digitalWrite(pin2, HIGH);
    digitalWrite(pin4, LOW);
    digitalWrite(pin7, LOW);
    delay(5000); // Wait for 5000 millisecond(s)
    digitalWrite(pin2, LOW);
    digitalWrite(pin4, HIGH);
    digitalWrite(pin7, LOW);
    delay(5000); // Wait for 5000 millisecond(s)
    digitalWrite(pin2, LOW);
    digitalWrite(pin4, LOW);
    digitalWrite(pin7, HIGH);
    delay(5000); // Wait for 5000 millisecond(s)
  }
  else
  {
  }
}
