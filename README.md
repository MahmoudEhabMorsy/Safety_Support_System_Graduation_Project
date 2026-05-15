# Safety Support System (ADAS) — Graduation Project

> An embedded systems and IoT-based Advanced Driver Assistance System (ADAS) designed to enhance vehicle safety through tire burst early detection, parking assistance, water cooling, steering lock control, and real-time mobile monitoring.

> **Note:** Some functionalities and simulations in this repository may require hardware components and specific embedded environments to run correctly.

---

# Overview

Safety Support System (ADAS) is a multidisciplinary graduation project developed at Ain Shams University by students from the Computer & Systems Engineering and Electronics & Communications Engineering departments.

The project combines:

- Embedded Systems
- IoT Communication
- Mobile Development
- Real-Time Monitoring
- Vehicle Safety Logic
- Sensor Integration
- Client-Server Architecture

The system aims to improve driving safety and reduce risks caused by tire failures, overheating, parking collisions, and unsafe vehicle conditions.

The solution consists of:

- Embedded control nodes
- Sensor-based monitoring systems
- IoT communication modules
- Mobile application
- Backend server
- Web dashboard
- Real-time data visualization

---

# Main Features

## Tire Burst Early Detection System (TBEDS)

Monitors tire pressure and temperature in real-time using sensors and predefined thresholds.

### Capabilities
- Detects dangerous tire conditions early
- Warns the driver before severe failure occurs
- Triggers safety procedures in critical conditions
- Helps reduce accidents caused by tire bursts

---

## Water Cooling System (WCS)

A cooling mechanism designed to reduce tire overheating.

### Capabilities
- Monitors tire temperature continuously
- Activates water cooling automatically
- Stops cooling once safe temperature levels are restored
- Improves tire longevity and performance

---

## Steering Lock System (SLS)

Safety mechanism responsible for handling severe tire conditions.

### Capabilities
- Limits unsafe vehicle movement
- Gradually slows down the vehicle
- Locks steering during dangerous situations
- Helps maintain vehicle stability

---

## Parking Assistance System (PAS)

Ultrasonic sensor-based parking assistance system.

### Capabilities
- Measures surrounding distances
- Detects nearby obstacles
- Provides visual and audible warnings
- Uses different warning levels based on proximity

---

## IoT Monitoring System

Cloud-connected monitoring system for real-time vehicle data.

### Capabilities
- Sends tire data to backend server
- GPS tracking support
- Real-time communication using Socket.io
- Mobile application integration
- Historical data and analytics

---

# System Architecture

The project is divided into three main embedded nodes:

## 1. Moving Control Node
Responsible for:
- Vehicle movement control
- Bluetooth communication
- PWM motor control
- Driver command handling

### Technologies
- ATmega32
- HC-05 Bluetooth Module
- UART Communication
- PWM Motor Drivers

---

## 2. Sensing Control Node
Responsible for:
- Tire pressure monitoring
- Temperature monitoring
- Parking assistance logic
- Water cooling activation
- Steering lock logic

### Technologies
- BMP180 Sensor
- Ultrasonic Sensors
- SPI Communication
- Buzzer & LED Indicators

---

## 3. IoT Node
Responsible for:
- Data aggregation
- GPS communication
- Server communication
- Wireless transmission

### Technologies
- ESP01 Wi-Fi Module
- GPS Module
- Socket Communication

---

# Software Components

## Mobile Application

A React Native mobile application that allows users to:

- View tire pressure and temperature
- Monitor vehicle status
- Receive alerts and warnings
- Access real-time car information
- Authenticate securely

### Stack
- React Native
- Socket.io Client
- AWS Amplify

---

## Backend Server

Handles communication between embedded systems and client applications.

### Responsibilities
- API management
- Authentication
- Real-time communication
- Database operations
- Data processing

### Stack
- Node.js
- Express.js
- Socket.io
- MongoDB

---

## Web Dashboard

Administrative dashboard used for:

- Adding vehicles
- Managing users
- Connecting cars to owners
- Monitoring system data

---

# Technologies Used

## Embedded Systems
- Embedded C
- AVR ATmega32
- UART
- SPI
- I2C (TWI)
- PWM
- Interrupts

## Sensors & Hardware
- BMP180 Pressure & Temperature Sensor
- HC-SR04 Ultrasonic Sensor
- HC-05 Bluetooth Module
- ESP01 Wi-Fi Module
- GPS Module
- DC Motors
- LEDs
- Buzzer
- Water Pump

## Software
- React Native
- Node.js
- Express.js
- MongoDB
- Socket.io
- JavaScript

## Tools
- Eclipse IDE
- GCC Compiler
- Proteus
- Visual Studio Code
- GitHub

---

# Repository Structure

```bash
.
├── Back/
│   ├── Moving Control Node
│   ├── Early Detection & Steering Lock & Water Cooling
│   └── Embedded Drivers & Modules
│
├── Last Version/
│   ├── Mobile Application
│   ├── Backend Server
│   ├── Web Dashboard
│   └── IoT Components
├── Documentation
└── README.md
```
---

# Communication Protocols

The system uses multiple communication protocols for reliable data exchange:

| Protocol | Usage |
|---|---|
| UART | Bluetooth & Serial Communication |
| SPI | Inter-node Communication |
| I2C (TWI) | Sensor Communication |
| Wi-Fi | IoT Communication |
| Socket.io | Real-Time Client Communication |

---

# Safety Logic

The system classifies tire conditions into three states:

## Safe State
- Normal operation
- No action required

## Moderate State
- Warning state
- Activates Early Detection System
- Alerts driver

## Severe State
- Critical condition
- Activates Steering Lock System
- Gradually stops vehicle safely

---

# Parking Assistance Logic

The Parking Assistance System classifies nearby obstacles into multiple risk levels:

- Safe Distance
- Low Risk
- Moderate Risk
- High Risk
- Extreme Risk

Different LED and buzzer behaviors are used for each level.

---

# Prototype Features

The prototype includes:

- Bluetooth-controlled RC vehicle
- Real-time tire monitoring
- Live server communication
- GPS tracking
- Parking assistance
- LED status indicators
- Safety response system
- Embedded multi-node architecture

---

# Testing

The project includes:

## Unit Testing
- BMP180 Sensor Testing
- Bluetooth Testing
- GPS Testing
- Ultrasonic Testing

## Integration Testing
- Node Communication Testing
- Safety Scenario Testing
- Parking Assistance Validation
- Real-Time Monitoring Validation

## Testing Modes

Custom testing modes were implemented to simulate:

- Early Detection System scenarios
- Water Cooling System scenarios
- Steering Lock System scenarios
- Default operational behavior

---

# How It Works

1. Sensors collect pressure, temperature, and distance data.
2. Embedded nodes process and classify readings.
3. Safety logic determines the current system state.
4. Critical data is transmitted to the IoT node.
5. The IoT node sends data to the backend server.
6. The mobile application receives live updates.
7. The system automatically reacts to dangerous conditions.

---

# Future Improvements

Potential future enhancements include:

- AI-based predictive tire analysis
- Machine learning anomaly detection
- Camera-based lane assistance
- Cloud analytics dashboard
- Autonomous parking capabilities
- CAN bus integration
- Real vehicle deployment
- Enhanced mobile UI/UX

---

# Academic Information

**University:** Ain Shams University  
**Faculty:** Faculty of Engineering  
**Departments:**
- Computer & Systems Engineering
- Electronics & Communications Engineering

**Project Type:** Graduation Project  
**Year:** 2023

---

# Team Members

- Ahmed Yasser
- Khaled Amr
- Mahmoud Abdellatif
- Mahmoud Ehab
- Mahmoud Fathy
- Mahmoud Khaled
- Mohamed Khaled
- Nour Atef
- Rady Magdy

---

# Supervisors

- Prof. Dr. Wagdy Anis
- Dr. Bassem Amin

---

# Mentorship

Mentored through the Valeo Mentorship Program.

---

# Key Learning Outcomes

This project involved practical experience with:

- Embedded systems architecture
- Real-time systems
- Automotive safety concepts
- IoT system integration
- Mobile application development
- Client-server communication
- Sensor interfacing
- Communication protocols
- System testing and validation
- Team collaboration using Agile methodologies

---

# Disclaimer

This project is an educational prototype developed for academic purposes.

It is not intended for production-grade automotive deployment without further safety validation, industrial testing, and certification.

---

# Acknowledgments

Special thanks to:

- Ain Shams University
- Faculty of Engineering
- Valeo Mentorship Program
- Project supervisors and mentors
- Open-source communities and contributors

---

## Demo

[Demo Video Link](https://drive.google.com/file/d/1kvOKJ2upMjnD_64EVGWJ5WimWvPmJH6b/view?usp=sharing)

## Screenshots
![Poster](https://drive.google.com/file/d/1MISAJeZmkSbfZGA5erI4NxcbU2n-J0fz/view?usp=drive_link)
![Mobile App](https://drive.google.com/drive/folders/1vL78CmYDWtqwqEOu0tVCRsxG0etwbRaD?usp=sharing)
![Prototype](https://drive.google.com/file/d/1URCmMvyHi9mWJXVDumhUIqFrQWPCdPdA/view?usp=drive_link)
![3D Layer](https://drive.google.com/file/d/1f_geCe_TqUUhsccbi-K23QVT2TnF0Rxv/view?usp=sharing)
