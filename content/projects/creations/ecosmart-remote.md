---
title: EcoSmart Remote
date: 2018-07-05
image: /img/circleci-workflow.png
link: https://github.com/PhilRW/ecosmart-remote
image: /images/nodemcu.jpg
description: Embedded firmware remote interface for tankless water heater
tags:
- C
- CLion
- embedded
- ESP8266
- IoT
- hacking
- reverse engineering
- protocols
- GitHub
fact: 
featured: true
weight: 500
---
The objective was to create a remote control interface for the [EcoSmart electric tankless water heater](https://www.ecosmartus.com/). The remote they manufactured had been discontinued and there was no documentation available on the interface protocol.

Fortunately [another engineer](https://electronics.stackexchange.com/questions/233374/reverse-engineering-asynchronous-serial-protocol-for-ecosmart-tankless-water-hea) had scoped out the I/O pins enough to [bit bang](https://en.wikipedia.org/wiki/Bit_banging) some control, but I wanted to go further into the protocol.

I was able to reverse engineer the TTL protocol control and status bits using an IR library and determined which were for system on/off, Fahrenheit/Celsius, and water flow detected on/off. I implemented the protocol transceiver as a new class of that library and wrapped it in some code to connect the [ESP8266](https://en.wikipedia.org/wiki/ESP8266) [NodeMCU](https://en.wikipedia.org/wiki/NodeMCU) device to the [home automation](https://www.home-assistant.io/) system's [MQTT](https://en.wikipedia.org/wiki/MQTT) broker.

This was a component of a larger project to [refit the domestic hot water system](https://blog.rosenberg-watt.com/2018/08/01/towards-better-domestic-hot-water/) in my house.
