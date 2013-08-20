---
layout : post
title : MQTT Java Publisher and Subscriber using Eclipse Paho
category : MQTT 
tags : MQTT
---

MQTT is a one of most popular machine-to-machine (M2M) connectivity protocol. It was designed with extremely lightweight that support embedded and low power processing device. MQTT popularly used in samrtphone chat application and sensor communication. 
You can find more information about MQTT from here. MQTT is broker based message queuing system. It is very to install open Source MQTT server like Mosquitto using a simple apt-get or yum command.
    
    sudo apt-get install mosquitto


Eclipse Paho is one mqtt client work well with mosquitto. The below MQTT subscriber and publisher code based on java eclipse paho library 1.0.1. You can also use public mosquitto server in <a href='http://test.mosquitto.org/'>test.mosquitto.org</a>

Checkout the complete source for MQTT subscriber and publisher from <a href="https://bitbucket.org/mkjinesh/mqttclient">here</a>
