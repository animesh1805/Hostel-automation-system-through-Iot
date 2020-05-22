#define BLYNK_PRINT Serial
#include <ESP8266WiFi.h>
#include <BlynkSimpleEsp8266.h>
int pirPin = 14;
int relayPin = 5;
int pirValue;

char auth[] = "XuFyIlmQbb32kdaOC3Od3q-M34sjuPO5";

char ssid[] = "VenomZone";
char pass[] = "aman12346";

void setup()
{
  Serial.begin(115200);
  Blynk.begin(auth, ssid, pass);
  pinMode(pirPin, INPUT);
  pinMode(relayPin, OUTPUT);
}

void pirSensor()
{
  pirValue = digitalRead(pirPin);
  Blynk.virtualWrite(V0, pirValue);
}

void loop()
{
  Blynk.run();
  pirSensor();
  if (pirValue == HIGH)
  {
    digitalWrite(relayPin, LOW);
  }
  
  else
  digitalWrite(relayPin, HIGH); 
}
