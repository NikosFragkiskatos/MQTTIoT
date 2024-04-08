# ThingsBoard IoT Project with Mosquitto MQTT

## Introduction

This project showcases a real-time IoT application using ThingsBoard, Google's Firebase DB, and Mosquitto MQTT to produce and consume hypothetical sensor data. The Internet of Things (IoT) is revolutionizing the way we interact with the physical world. Through sensors and connectivity, everyday objects can communicate and perform tasks, making environments smarter and more responsive. In this project, we demonstrate the integration of sensor data with ThingsBoard, an IoT platform that provides device management, data collection, processing, and visualization, all essential components in the IoT ecosystem. This is part of the practical coursework I completed for the MIT Data Engineering program.  

In the files of this project, you will find also two word files; Part1-GeneralSetup, and Part2-AlarmSetup. Those files include screenshots of the execution of the project and describe details of the steps taken.

## Installation
  
### Part 1: Mosquitto MQTT Broker Setup
Ensure Docker is installed and running. Use the provided `docker-compose.yml` to set up the Mosquitto MQTT broker.

### Part 2: ThingsBoard Setup
Access your ThingsBoard instance and configure it to display sensor data from the MQTT broker.

### Prerequisites
- Docker for running the Mosquitto MQTT broker
- Python 3.x for running the data publisher script
- Node.js for the server-side consumption of MQTT data
- Access to a ThingsBoard instance
  
### Installation
1. Clone the repository:  
`git clone https://github.com/NikosFragkiskatos/MQTTIoT.git`  

2. Start the Mosquitto MQTT broker with Docker:
`docker-compose -f docker-compose.yml up -d`

3. Install the required Python libraries for publishing sensor data:
`pip install paho-mqtt`

4. Navigate to the project directory and install node.js dependencies.
`npm install`

### Usage  
#### Starting the MQTT Publisher  
Execute the `TBPublish.py` script to publish sensor data:  
`python TBpublish.py`  

