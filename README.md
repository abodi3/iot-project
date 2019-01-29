iot-project
===========

Mqtt protocol and Azure iot hub.

### About

This project uses Mqtt protocol, Azure iot hub, Node Red, raspberrypi, arduino with a temperature sensor to create a mini iot solution by monitoring the room temperature. The arduino sends the data from the sensor to the node red using the standard firmata example.
Temperature is calculated from the sensor values. The calculated temperature is saved in a database using mysql, and published to local mosquitto mqtt broker on the raspberry pi and also to Azure iot hub. There are two led lights simulating heating and cooling systems connected to digital pins 9 and 10 of the arduino. These led lights subscribe to the broker and receive temperature updates and hence light up or off when conditions are met. 
There is also weather forecast which is polled from openweathermaps.org 
The weather information is also published to the local broker. 
The nodered dashboard website presents a user interface from which the user can interact with the project. For example manually putting the leds on or off without the need for mqtt subscribe conditions to be met. Also weather forecast and current temperature is readily available. 
