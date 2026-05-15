# Adiuno_Obstacle_avoidance_Car
# Arduino Obstacle Avoidance Car
A simple 4WD obstacle avoidance car built from scratch as part of my robotics foundation learning.

## 🛠️ Hardware Used
- Arduino Uno R3
- Integrated L298N 4WD motor driver board
- 4x DC gear motors
- 4x Wheels
- HC-SR04 ultrasonic sensor
- 2x 18650 3.7V batteries
- Acrylic chassis

## 📝 Software
- Arduino IDE 2.0+
- No external libraries required

## 🔌 Wiring Diagram
| Component | Arduino Pin |
|-----------|-------------|
| IN1       | 4           |
| IN2       | 5           |
| IN3       | 6           |
| IN4       | 7           |
| ENA       | 9           |
| ENB       | 10          |
| HC-SR04 Trig | 12      |
| HC-SR04 Echo | 13      |
| VCC       | 5V          |
| GND       | GND         |

## 🚗 How It Works
1. The HC-SR04 sensor measures the distance to obstacles in front of the car
2. If an obstacle is detected within 20cm:
   - The car stops immediately
   - It backs up for 0.6 seconds
   - It turns right for 0.6 seconds
3. If no obstacle is detected: the car moves forward continuously

## 📚 What I Learned
- How DC motors work and how to control them with an H-bridge
- How ultrasonic sensors measure distance using sound waves
- Differential steering for 4WD vehicles
- How to write clean, modular code with functions
- The importance of debugging hardware and software together

## 🚀 Next Steps
- Add servo motor to scan left and right for better obstacle detection
- Implement PID control for smoother movement
- Connect to ROS for more advanced robotics
- Integrate reinforcement learning for autonomous navigation

## Author
陈韬 | First-year Mechanical Engineering, Donghua University
