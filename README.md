# smart-home-iot-platform
Plug-and-play IoT home automation system with energy monitoring, MQTT integration and thermal prediction.


# SmartHome

A modular plug-and-play home automation platform developed as part of the Electrical and Computer Engineering degree at the University of Coimbra.

The project was designed to provide an accessible and scalable smart home ecosystem, integrating climate control, energy management and predictive intelligence through Home Assistant and MQTT.

---

## Overview

SmartHome is divided into two main subsystems:

### SmartClima

An intelligent climate control solution designed for traditional Portuguese gas central heating systems.

The system consists of multiple ESP32-C6-based modules capable of autonomous configuration, Home Assistant integration and remote operation.

### SmartPlug

A smart power outlet focused on remote device control and real-time energy monitoring.

The module provides energy consumption monitoring, load automation via scheduling, and improved energy efficiency through the integration of PID control and AI within Home Assistant.

---

## System Architecture

The platform follows a modular architecture based on:

- ESP32-C6 microcontrollers
- MQTT communication protocol
- Raspberry Pi-Based Central Server
- Home Assistant
- Python-based AI model
- Wi-Fi connectivity

All automation logic is implemented within Home Assistant, making the system highly configurable and easy to extend.

---

# SmartClima

## Objective

To modernize traditional domestic heating systems through intelligent temperature monitoring, remote control, and thermal prediction, integrating PID-based control with a stepper motor for automated actuation of a conventional residential radiator valve.

## Main Components

### Control Module

The main control module, designed to replace a traditional residential thermostat, is composed of:

- ESP32-C6
- Relay
- Status LED
- Configuration reset button

#### Features

- Automatic Wi-Fi provisioning
- Plug-and-play installation
- MQTT communication
- Home Assistant auto-discovery
- Visual status feedback through LED indicators

During the first setup, the module creates its own Wi-Fi network.

The user connects to this network and provides local Wi-Fi credentials through a configuration interface.

After connecting to the local network, the device automatically:

1. Connects to the MQTT broker.
2. Registers itself through MQTT Discovery.
3. Appears automatically inside Home Assistant.

### Temperature Sensor Module

The environmental sensing module consists of:

- ESP32-C6
- DHT11 temperature
- Status LED
- Reset button

Although the DHT11 was used for prototyping purposes, more accurate sensors would be preferable for production environments.

### Valve Actuation Module

Responsible for controlling heating flow.

Components:

- ESP32-C6
- Stepper motor
- End-stop microswitch
- Status LED
- Reset button

#### Features

- Valve positioning control (0-100%)
- Homing procedure using microswitch
- Remote actuation
- Integration with Home Assistant automations

---

# SmartPlug

## Objective

To provide remote control and real-time monitoring of electrical loads.

## Components

- PZEM-004T (electronic sensor module used to measure AC electrical energy parameters)
- ESP32-C6
- Status LED
- Configuration reset button
- Plug
- Relay

## Features

- Remote ON/OFF control
- Energy consumption monitoring
- Power measurement
- Supply voltage measurement
- MQTT communication
- Automation support
- Automatic Wi-Fi provisioning
- Plug-and-play installation
- Home Assistant auto-discovery
- Visual status feedback through LED indicators

The SmartPlug enables users to monitor energy consumption patterns and remotely control connected loads through Home Assistant.

### Demonstration Video

[▶ Watch the SmartPlug Demo](SmartPlug/Documentation/videos/smartplug-demo.mp4)

---

# Artificial Intelligence

The platform includes a thermal prediction model developed in Python and executed directly within Home Assistant.

The model was designed to:

- Predict room temperature evolution considering outside temperature
- Improve heating efficiency
- Anticipate thermal behaviour
- Support automated climate control decisions
- Learn the heating patterns of the dwelling

---

# Home Assistant Integration

Home Assistant acts as the central management platform.

All system logic is implemented through:

- MQTT Discovery
- Entities
- Scripts
- Automations
- Dashboards

This approach allows the system to operate without dedicated backend servers while remaining highly customizable.

---

# Technologies

## Hardware

- ESP32-C6
- Relay modules
- DHT11
- Stepper motor
- Microswitches
- Switches
- LED's

## Software

- C++
- Python
- MQTT
- Home Assistant
- Yaml
- Jinja2

---

# Project Outcomes

- Successful development of a modular home automation ecosystem.
- Automatic device discovery and provisioning.
- Remote climate control.
- Energy monitoring and management.
- Thermal prediction using machine learning techniques.
- Full integration with Home Assistant.

---

# Future Improvements

- Replace DHT11 with higher accuracy sensors.
- Add OTA firmware updates.
- Improve thermal prediction models.
- Develop custom PCB designs.
- Make a 3D-printed enclosure for each module.
- Support additional smart home devices.
