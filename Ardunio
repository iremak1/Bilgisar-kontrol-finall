int trigPin = 12;
int echoPin = 11;
unsigned long duration, cm;
int buzzerPin = 8;

void setup() {
  Serial.begin(9600);
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  pinMode(buzzerPin, OUTPUT); 
}

void loop() {
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

  duration = pulseIn(echoPin, HIGH);
  cm = (duration / 2) / 29.1;

  if (cm >= 0 && cm <= 100) {
    tone(buzzerPin, 1000); 
  } else {
    noTone(buzzerPin); 
  }

  delay(500);
}
