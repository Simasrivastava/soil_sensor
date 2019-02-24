# soil_sensor
int a = A0;


void setup() {
  pinMode(a, INPUT);
  Serial.begin(9600);
  }

void loop() {
  int val = analogRead(a);
  int per = map(val, 0, 1023, 100, 0);
  Serial.print("MOISTER Status : ");
  Serial.print(per);
  Serial.println("%");
  
  delay(100);
}
