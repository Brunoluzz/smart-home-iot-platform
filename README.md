# smart-home-iot-platform
Plug-and-play IoT home automation system with energy monitoring, MQTT integration and thermal prediction.


# SmartHome

A modular plug-and-play home automation platform developed as part of the Electrical and Computer Engineering degree at the University of Coimbra.

The project was designed to provide an accessible and scalable smart home ecosystem, integrating climate control, energy management and predictive intelligence through Home Assistant and MQTT.

---

## Overview

SmartHome is divided into two main subsystems:

### SmartClima

An intelligent climate control solution designed for traditional Portuguese central heating systems.

The system consists of multiple ESP32-based modules capable of autonomous configuration, Home Assistant integration and remote operation.

### SmartPlug

A smart power outlet focused on remote device control and real-time energy monitoring.

The module allows users to monitor consumption, automate loads and improve energy efficiency through Home Assistant.

---

## System Architecture

The platform follows a modular architecture based on:

- ESP32 microcontrollers
- MQTT communication protocol
- Home Assistant
- Python-based AI models
- Wi-Fi connectivity

All automation logic is implemented within Home Assistant, making the system highly configurable and easy to extend.

---

# SmartClima

## Objective

To modernize traditional domestic heating systems by enabling intelligent temperature monitoring, remote control and thermal prediction.

## Main Components

### Control Module

The main control module is composed of:

- ESP32
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

- ESP32
- DHT11 temperature and humidity sensor
- Status LED
- Reset button

Although the DHT11 was used for prototyping purposes, more accurate sensors would be preferable for production environments.

### Valve Actuation Module

Responsible for controlling heating flow.

Components:

- ESP32
- Stepper motor
- End-stop microswitch
- Status LED
- Reset button

#### Features

- Valve positioning control
- Homing procedure using microswitch
- Remote actuation
- Integration with Home Assistant automations

---

# SmartPlug

## Objective

To provide remote control and real-time monitoring of electrical loads.

## Features

- Remote ON/OFF control
- Energy consumption monitoring
- Power measurement
- Integration with Home Assistant
- MQTT communication
- Automation support

The SmartPlug enables users to visualize consumption patterns and implement energy-saving strategies through Home Assistant.

---

# Artificial Intelligence

The platform includes a thermal prediction model developed in Python and executed directly within Home Assistant.

The model was designed to:

- Predict room temperature evolution
- Improve heating efficiency
- Anticipate thermal behaviour
- Support automated climate control decisions

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

- ESP32
- Relay modules
- DHT11
- Stepper motor
- Microswitches

## Software

- C++
- Python
- MQTT
- Home Assistant

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
- Support additional smart home devices.
