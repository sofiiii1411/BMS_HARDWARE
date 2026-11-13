# BMS SentinelAI-X Hardware

Hardware implementation and firmware architecture for the **Building Management System (BMS) SentinelAI-X**.

## Project Architecture

```
BMS HARDWARE/
└── BMS_SENTINELAI-X/
    ├── DOCUMENTATION/
    │   ├── CIRCUIT_DIAGRAMS/
    │   ├── HARDWARE_DOCUMENTATION/
    │   ├── PIN_CONFIGURATION/
    │   └── PROJECT_REPORT/
    ├── HARDWARE/
    │   ├── ROOM101_ECOSPACE/
    │   │   ├── include/ (room101_config.h, room101_pins.h)
    │   │   ├── lib/ (Actuators, Displays, Energy Monitoring, ESP32-CAM, Sensors, etc.)
    │   │   ├── src/
    │   │   └── platformio.ini
    │   ├── ROOM201_SECURELAB/
    │   │   ├── include/
    │   │   ├── lib/ (Actuators, Displays, ESP32-CAM, Sensors, etc.)
    │   │   ├── src/
    │   │   └── platformio.ini
    │   └── SHARED_HARDWARE/
    │       ├── COMMUNICATION/ (MQTT & WiFi Manager)
    │       └── RELAY_MODULE/ (4-Channel Relay)
    └── README.md
```

## Features & Modules

- **Room 101 (EcoSpace)**:
  - Sensors: DHT (Temp/Humidity), LDR (Light), MQ (Gas/Air Quality), PIR (Motion)
  - Actuators: DC Motor, Cooling Fan, Motor Controller, Servo Motor
  - Displays & Peripherals: LCD, 2.4" TFT, PZEM Energy Monitor, ESP32-CAM, Indicators, Power Management
- **Room 201 (SecureLab)**:
  - Sensors: DHT, LDR, MQ, PIR, Ultrasonic, Vibration
  - Actuators: DC Motor, Fan, Motor Controller, Servo Motor
  - Displays & Peripherals: 1.8" TFT, ESP32-CAM, Indicators, Power Management
- **Shared Hardware & Connectivity**:
  - MQTT Communication client
  - WiFi Manager for dynamic provisioning
  - 4-Channel Relay Control
