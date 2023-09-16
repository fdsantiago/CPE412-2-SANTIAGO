# Analog-IO
Fernand D. Santiago - Analog-IO - Exercse

void setup() {
  pinMode(13, OUTPUT);
  pinMode(A0, INPUT);
  Serial.begin(9600);
}

void loop() {
  // Read the value from the potentiometer (0-1023)
  int potValue = analogRead(A0);
  
  // potValue Map
  int delayTime = map(potValue, 0, 1023, 10, 1000);

  // Turn the LED on
  digitalWrite(13, HIGH);

  // Delay for the calculated delay time
  delay(delayTime);

  // Turn the LED off
  digitalWrite(13, LOW);
  
  // Print potValue
  Serial.println(potValue);

  // Delay for the same amount of time
  delay(delayTime);
}

