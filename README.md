# HOME-AUTOMATION-WITH-BLUETOOTH
"Company": CODTECH IT SOLUTION
"NAME": GANAVI AL
"INTERN ID" :CT04DG130
"DOMAIN": EMBEDDED SYSTEM
"DURATION": 4 WEEKS
"MENTO": NEELA SANTHOS

🔌 Bluetooth-Controlled Home Automation System (CODTECH Task-2)
💡 Overview
This project is part of my internship at CODTECH IT SOLUTIONS PVT. LTD under the domain of Embedded Systems. The goal of this task is to build and simulate a Bluetooth-based home automation system using Arduino UNO. Since the Tinkercad platform does not support the HC-05 Bluetooth module, the project uses the Serial Monitor to simulate Bluetooth commands.

🎯 Objectives
Simulate a Bluetooth-controlled system to switch devices ON/OFF
Use serial communication to replicate Bluetooth behavior
Learn embedded system design using Arduino and Tinkercad
Develop logic for appliance control using commands

🧰 Components Used
Arduino UNO
2x LEDs (simulate appliances)
2x 220Ω resistors
Breadboard
Jumper wires
Serial Monitor (as Bluetooth substitute)

🔌 Circuit Connections
Arduino Pin	Connection
Pin 7	Resistor → Anode of LED1 → GND
Pin 8	Resistor → Anode of LED2 → GND
GND	Connected to breadboard GND rail

💻 Arduino Code
cpp
Copy
Edit
char btData;

void setup() {
  Serial.begin(9600);
  pinMode(7, OUTPUT);
  pinMode(8, OUTPUT);
}

void loop() {
  if (Serial.available()) {
    btData = Serial.read();

    if (btData == 'A') digitalWrite(7, HIGH); // Turn ON LED1
    if (btData == 'a') digitalWrite(7, LOW);  // Turn OFF LED1

    if (btData == 'B') digitalWrite(8, HIGH); // Turn ON LED2
    if (btData == 'b') digitalWrite(8, LOW);  // Turn OFF LED2
  }
}
📺 How to Simulate in Tinkercad
Go to Tinkercad Circuits
Add Arduino UNO, 2 LEDs, 2 resistors, and a breadboard
Make connections as per the table above
Paste the Arduino code into the text editor
Start Simulation
Open Serial Monitor and type the following commands:

A → Turn ON LED1

a → Turn OFF LED1

B → Turn ON LED2

b → Turn OFF LED2

📝 Note
Since HC-05 Bluetooth modules are not available in Tinkercad, the project uses the Serial Monitor to simulate Bluetooth communication. The logic and functionality are equivalent to a real-world Bluetooth-controlled system.
