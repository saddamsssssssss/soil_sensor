int humedad = 0;

void setup()
{
  pinMode(A1, INPUT);
  Serial.begin(9600);
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
}

void loop()
{
  humedad = analogRead(A1);
  Serial.println(humedad);
  delay(200);
  if (humedad <= 500) {
    digitalWrite(13, HIGH);
    digitalWrite(12, LOW);
  } else {
    digitalWrite(13, LOW);
    digitalWrite(12, HIGH);
  }
}

![image](https://github.com/saddamsssssssss/soil_sensor/assets/139205268/ba968a0f-1196-4c80-84e7-3ba5cd8588e2)
