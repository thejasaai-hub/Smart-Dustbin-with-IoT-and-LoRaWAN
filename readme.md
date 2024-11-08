# Smart Dustbin with IoT and LoRaWAN

## Overview
The **Smart Dustbin** project aims to improve waste management through real-time monitoring of waste levels and optimizing waste collection routes. This system utilizes IoT technology with LoRaWAN for long-range data transmission, enabling remote monitoring of dustbin fill levels. When the dustbin reaches a predefined capacity, a notification is sent to a central server via the Arduino IoT Cloud, allowing waste management authorities to plan and optimize collection schedules, reducing unnecessary collection trips and environmental impact.

## Key Features
- **Real-Time Monitoring**: Ultrasonic sensors measure the fill level of the dustbin and automatically open/close the lid using a servo motor.
- **Remote Alerts**: When the dustbin is full, alerts are sent via LoRaWAN to a central server, which notifies authorities through the Arduino IoT Cloud.
- **IoT Integration**: Data is transmitted to the Blynk IoT mobile application for real-time monitoring and notifications.
- **Environmental Impact**: Reduces unnecessary waste collection trips, saving fuel and reducing emissions.

## Components Used
- **ESP32**: Primary microcontroller for handling sensor data and controlling the servo motor.
- **LoRaWAN Modules**: Used for long-range communication to transmit data to the server.
- **Ultrasonic Sensor**: Measures the distance to detect the fill level of the dustbin.
- **Servo Motor**: Opens and closes the lid of the dustbin based on the fill level.
- **MKR GPS Module**: Provides location data for each dustbin.
- **Arduino IoT Cloud**: Platform for remote monitoring and control.
- **Blynk IoT App**: Mobile application for real-time monitoring and alerts.

## System Architecture

### Block Diagram
The system architecture includes the integration of ESP32, ultrasonic sensors, servo motor, GPS module, and Arduino IoT Cloud, as illustrated below:

![Block Diagram](BLOCK_DIAGRAM.png)

### Project Workflow
1. **Sensor Detection**: The ultrasonic sensor detects the fill level inside the dustbin.
2. **Lid Operation**: The servo motor automatically opens/closes the lid based on proximity.
3. **Data Transmission**: When full, data is transmitted through LoRaWAN to the Arduino IoT Cloud.
4. **Notification**: The Blynk IoT app receives alerts, notifying waste management authorities.

## Setup and Usage

### Prerequisites
- **Arduino IDE**: Used for programming the ESP32 and LoRaWAN modules.
- **Required Libraries**:
  - `Servo` for servo motor control.
  - `Ultrasonic` for ultrasonic sensor data.
  - `Arduino_MKRGPS` for GPS functionality.

### Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/Smart-Dustbin.git

2. **Upload Code**:

-Open PROJECT_CODE.txt in the Arduino IDE.
-Install the required libraries using the Library Manager.
-Upload the code to the ESP32.

3. **Setup Blynk IoT**:

Configure the Blynk IoT app to work with the Arduino IoT Cloud, enabling it to receive notifications about the dustbin fill level.

