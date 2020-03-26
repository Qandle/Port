#define relay 4

const int sensorPin = A0;  // sensor input pin 
int moisture = 0;// variable to store the value coming from the sensor 


void setup() { 
  Serial.begin(9600); 
  pinMode(relay, OUTPUT); 

} 

void loop() { 
  // read the value from the sensor 
  moisture = analogRead(sensorPin); 
  Serial.print("Soil Moisture = "); 
  Serial.println(moisture); 
   
  if(moisture>900){ 
    Serial.println("Sensor in Air"); 
  } 
  else if (moisture > 700 && moisture < 900){ 
    Serial.println("Sensor in dry soil"); 
  } 
  else if (moisture>500 && moisture < 700) { 
    Serial.println("Sensor in humid soil"); 
  } 
  else if (moisture<500){ 
    Serial.println("Sensor in water"); 
  } 
  delay(500); 

 if (moisture>700 && moisture <900) { 
    digitalWrite(relay, LOW); 
    Serial.println("Work"); 

  } 

  else { 
    digitalWrite(relay, HIGH); 
    Serial.println("Stop");
  } 
  
  delay(1000);

}
