# Guardian-IoT
# Guardian IoT – A Smart Safety System for Preventing Septic Tank Fatalities

## Overview

Guardian IoT is an IoT-based septic tank safety and monitoring system designed to reduce the risks faced by sanitation workers during septic tank maintenance.

Septic tanks can contain hazardous gases, oxygen-deficient environments and high temperatures. Traditional monitoring systems often focus primarily on gas detection and alerts, without providing active measures to improve the internal air quality.

Guardian IoT addresses these limitations through sensor-based environmental monitoring, real-time alerts, remote mobile monitoring and automated ventilation mechanisms.

## Problem Statement

Septic tank maintenance exposes workers to potentially hazardous conditions caused by toxic gases, insufficient oxygen and poor ventilation.

Existing systems may provide warnings when dangerous gases are detected but often lack oxygen monitoring, automated air-quality improvement and remote monitoring across multiple installations.

Guardian IoT aims to provide an integrated, cost-effective solution that identifies unsafe conditions and initiates preventive actions.

## Key Features

- **Multi-gas monitoring:** Detection of hazardous gases such as methane, hydrogen sulphide, ammonia, carbon monoxide and carbon dioxide.
- **Oxygen monitoring:** Monitoring oxygen levels to identify potentially unsafe oxygen-deficient conditions.
- **Environmental monitoring:** Temperature and humidity measurement inside the septic tank.
- **Real-time alerts:** Notifications when sensor readings cross configured safety thresholds.
- **Mobile monitoring:** Remote access to sensor readings and safety status through a mobile application.
- **Device identification:** Monitoring individual septic tank installations using unique IDs or location-based identification.
- **Automated ventilation:** An exhaust fan helps introduce fresh air into the tank.
- **Gas extraction:** A suction pump helps remove hazardous gases from the tank.

## System Architecture

The system follows a sensor-to-controller-to-monitoring-and-control architecture.

1. **Sensing Layer:** Gas, oxygen, temperature and humidity sensors collect environmental readings.
2. **Processing Layer:** The ESP32 microcontroller receives sensor data and evaluates readings against configured thresholds.
3. **Communication Layer:** Sensor information is transmitted for remote monitoring through the communication interface.
4. **Monitoring Layer:** The mobile application displays readings, device information and safety alerts.
5. **Control Layer:** The controller activates the suction pump and exhaust fan when configured hazardous conditions are detected.

### Working Flow

Sensor Data → ESP32 → Threshold Evaluation → Alert Generation → Pump and Fan Activation → Environmental Monitoring

## Hardware Components

| Component | Purpose |
|---|---|
| ESP32 | Main microcontroller and system controller |
| MQ-4 | Methane detection |
| MQ-135 | Ammonia and general air-quality detection |
| MQ-7 | Carbon monoxide detection |
| MQ-136 | Hydrogen sulphide detection |
| MG-811 | Carbon dioxide detection |
| ZE07-O2 or equivalent | Oxygen-level monitoring |
| DHT11 / DHT22 | Temperature and humidity monitoring |
| DC Suction Pump | Hazardous gas extraction |
| Exhaust Fan | Ventilation and fresh-air supply |

*Note: This is the component set documented in the project paper. The final list of physically integrated components should be updated to match the actual prototype.*

## Software and Technologies

- ESP32 Microcontroller
- Embedded C/C++
- Internet of Things (IoT)
- Sensor Data Acquisition and Processing
- Threshold-Based Alert and Control Logic
- Mobile Application
- Remote Monitoring and Communication

## Implementation and Testing

The proposed system architecture was evaluated in a controlled test environment simulating septic tank conditions.

The evaluation covered:

- Sensor readings under varying environmental conditions.
- Detection of configured hazardous conditions.
- Generation and delivery of mobile alerts.
- Activation of the suction pump and exhaust fan.
- Changes in gas readings following ventilation.
- Remote monitoring through the mobile application.

The project paper reports successful detection and alert generation in the controlled test setup, along with improvements in monitored gas conditions after ventilation was activated.

## Deployment Models

Guardian IoT proposes two deployment configurations:

**1. Comprehensive Septic Tank Safety System**

Designed for larger or community-level installations, incorporating sensors, a suction pump, an exhaust fan and mobile monitoring.

**2. Household Septic Tank Safety System**

A simplified, lower-cost configuration intended for household septic tanks, incorporating essential sensors and an exhaust fan.

## Project Contributors

- **Lingeshram S R** – Department of Electrical and Electronics Engineering (VLSI Design and Technology)
- **Pooja S** – Department of Electrical and Electronics Engineering (VLSI Design and Technology)
- **P U Nishwitha** – Department of Artificial Intelligence and Data Science
- **Faculty Guide:** B Manimaran, Assistant Professor, Department of Electronics and Communication Engineering

**Institution:** Rajalakshmi Institute of Technology, Chennai, India.

## Project Objective

To develop an affordable, IoT-enabled safety solution that supports early hazard detection, remote monitoring and preventive ventilation, helping improve safety during septic tank maintenance.

## Acknowledgements

This project was developed as a collaborative interdisciplinary initiative involving students from Artificial Intelligence and Data Science, VLSI Design and Technology, and Electronics and Communication Engineering.

---

**Project:** Guardian IoT  
**Category:** Internet of Things | Embedded Systems | Public Safety  
**Development Status:** Research and Prototype Development
