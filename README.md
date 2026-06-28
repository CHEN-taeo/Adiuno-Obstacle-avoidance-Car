# Arduino Obstacle Avoidance Car

<p align="center">
  <b>Autonomous navigation robot — ultrasonic obstacle detection with Arduino</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Arduino_Uno_R3-00979D?logo=arduino" alt="Arduino">
  <img src="https://img.shields.io/badge/License-MIT-green" alt="License">
  <img src="https://img.shields.io/github/last-commit/CHEN-taeo/Adiuno-Obstacle-avoidance-Car" alt="Last Commit">
</p>

---

## Overview

An Arduino-based autonomous obstacle avoidance car. Implements real-time ultrasonic sensing with servo-directed scanning and 4WD motor control for smooth navigation.

## Hardware

| Component | Specification |
|-----------|--------------|
| **Main Controller** | Arduino Uno R3 |
| **Drive Board** | Integrated 4WD motor driver |
| **Power** | Lithium battery pack |
| **Chassis** | 4WD with DC reduction motors |
| **Sensors** | Ultrasonic (HC-SR04) |
| **Total Cost** | ~300 RMB |

## Pin Configuration

| Function | Pin |
|----------|-----|
| LEFT_FORWARD | 4 |
| LEFT_BACKWARD | 2 |
| RIGHT_FORWARD | 8 |
| RIGHT_BACKWARD | 7 |

## Capabilities

- [x] Four-wheel forward / backward movement
- [x] In-place left / right rotation
- [x] Stable cycle operation (chassis foundation)
- [ ] HC-SR04 ultrasonic sensor integration (planned)
- [ ] Servo motor for dynamic sensor scanning (planned)

## Getting Started

1. Assemble hardware following the pin configuration above
2. Upload the Arduino sketch via Arduino IDE (2.x recommended)
3. Power on and test basic movement
4. Calibrate sensor thresholds for your environment

## Future Roadmap

- Ultrasonic sensor integration for automatic obstacle avoidance
- Power supply optimization for increased current capacity
- Servo motor integration for dynamic sensor direction control
- Bluetooth / WiFi remote control module

## License

MIT
