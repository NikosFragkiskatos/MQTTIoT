# ThingsBoard IoT Project with Mosquitto MQTT

This project is a comprehensive demonstration of real-time data streaming and analysis using ThingsBoard, an open-source IoT platform, and Mosquitto MQTT, an open-source message broker. The Internet of Things (IoT) is expanding rapidly, connecting devices and allowing them to interact in innovative ways. This project is divided into two parts: In Part 1, we set up an environment to produce, publish, and send temperature and humidity data to ThingsBoard and Firebase. Part 2 expands upon this by adding an alarm rule chain in ThingsBoard to monitor data against a threshold and send notifications to Firebase. This is part of my coursework submission for the MIT Data Engineering program.

## Part 1: Streaming Live Data to ThingsBoard

### Prerequisites
- Docker for running Mosquitto and ThingsBoard
- Python 3.x for running the publisher script
- Access to a ThingsBoard instance
- Access to Firebase for data storage

### Installation & Setup
1. **Mosquitto MQTT Broker Setup:**
   - Prepare the `Project_24_Docker` folder structure as specified and place the `docker-compose.yml` file accordingly.
   - Use Docker to initialize the Mosquitto MQTT broker.

2. **Paho MQTT Client Library:**
   - Install the `paho-mqtt` Python client library for MQTT communication.

3. **ThingsBoard & Firebase Configuration:**
   - Configure ThingsBoard and Firebase to display sensor data and create a `temperature` field in Firebase Realtime Database.

### Usage
1. **Run MQTT Publisher:**
   - Execute the `TBPublish.py` script to simulate the publishing of temperature and humidity data.

2. **ThingsBoard Data Visualization:**
   - Verify that the ThingsBoard instance is receiving data from the MQTT broker and visualize it on the dashboard.

## Part 2: Analyzing Live Streaming Data Using ThingsBoard

### Setup
1. **Firebase Alarm Configuration:**
   - In Firebase, create an `alarms` field and set its initial value to zero.

2. **ThingsBoard Alarm Rule Chains:**
   - In ThingsBoard, create and configure the `CreateAndClearAlarms`, `TempToFirebase`, and `AlarmToFirebase` rule chains as specified.
   - Set up API call nodes within these rule chains to post data to the corresponding fields in Firebase Realtime Database.

### Usage
1. **Integrate Rule Chains:**
   - Integrate the `CreateAndClearAlarms` rule chain into the Root Rule Chain in ThingsBoard and verify the setup.

2. **Monitor Firebase Realtime Database:**
   - Observe the `alarms` and `temperature` fields in Firebase for live updates triggered by the rule chains.

## Contributing
Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make to the MQTT and ThingsBoard project are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the `LICENSE.txt` file for details.

