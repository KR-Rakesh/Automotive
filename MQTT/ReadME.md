## MQTT

# WHAT IS MQTT?
MQTT (Message Queue Telemetry Transport) is a simple and ‘lightweight’ way for internet-connected devices to send each other messages.
This is important for RPC used in Automotive Telemetry. Where the Diagnostic information of vehicle like Speed,RPM,Location Service(GPS)etc., will 
transported via MQTT message techniques. Devices using MQTT communicate by publishing data to topics.
MQTT devices subscribe to a topic, and when data is published to that topic it is pushed to all the subscribers.

**Some of the important application of Automotive Telemetry are below.**
1.Vehicle tracking
2.Trailer tracking
3.Container tracking
4.Fleet management
5.Emergency warning system for vehicle
6.Intelligent vehicle technologies
7.Auto insurance / Usage-based insurance (UBI)

MQTT is considered as most reliable and secured data transmission techniques in AutomotiveIndustry.

**In this Example we’re going to set up an MQTT client on our raspberry pi which will subscribe to a couple of topics. Any data published to those topics will be pushed to our raspberry pi, and it can decide how to react.**

**Setup Required**
```
Python Version > 3
```

MQTT libraries to use with python
```
sudo pip install paho-mqtt
```

Now we’re going to Run a python script that sets the RasPi up as a client that connects to a free MQTT server.

Make sure your RasPi is connected to the internet.
We’re going to start our client. (I’ll refer to it as Terminal1). Enter:
```
python mqtt_client_demo.py
```

If everything goes well, you will shortly see a message saying Connected with result code 0

Open another terminal instance (I’ll refer to it as Terminal2).
```
python mqtt_publish_demo.py
```

Nothing much happens on Terminal2, but back over on Terminal1 we should see some action:
```
RakTest/test Hello
Received message #1, do something
RakTest/topic World!
Received message #2, do something else
```

You can also download MQTT tool available for  IOS and Android and try connecting to the MQTT HOST and PORT
```
MQTT Host:test.mosquitto.org"
MQTT Port: 1883
```
And start publish and receive the data. Maybe an alternative for **python mqtt_publish_demo.py.**