### *Reverse ProxiBrake with Ultrasonic Sensor and Motor Control*

This project involves building a reverse proximity brake system using an *ESP32* microcontroller, *ultrasonic sensor* (HC-SR04), *motor driver*, and various other components. The system detects objects behind a vehicle while reversing and triggers automatic braking to prevent accidents.

Key features:
- *Obstacle Detection*: Uses an ultrasonic sensor to measure distance from objects behind the vehicle.
- *Automatic Motor Control*: Stops the motors when an object is detected within a threshold distance (e.g., 5 cm).
- *Buzzer Alert*: A buzzer provides an audible alert when an obstacle is detected.
- *Manual Override*: A push button allows manual override of the system for 1 minute of motor operation, even with an obstacle present.
- *Safety Shutdown*: The buzzer is turned off for 1 minute when an obstacle is detected and resolved.

### *Components Used*:
- ESP32 Development Board
- Ultrasonic Sensor (HC-SR04)
- DC Motors and Motor Driver (L298N or similar)
- Push Button
- Buzzer
- Power Supply
- Jumper Wires

### *Pin Configuration*:
| Component           | ESP32 Pin        | Description                        |
|---------------------|------------------|------------------------------------|
| *Motor 1 IN1*     | GPIO 27          | Motor 1 Direction Control (IN1)    |
| *Motor 1 IN2*     | GPIO 26          | Motor 1 Direction Control (IN2)    |
| *Motor 1 ENA*     | GPIO 14          | Motor 1 Enable (ENA)              |
| *Motor 2 IN3*     | GPIO 25          | Motor 2 Direction Control (IN3)    |
| *Motor 2 IN4*     | GPIO 33          | Motor 2 Direction Control (IN4)    |
| *Motor 2 ENB*     | GPIO 32          | Motor 2 Enable (ENB)              |
| *Ultrasonic TRIG* | GPIO 12          | Trigger Pin for Ultrasonic Sensor |
| *Ultrasonic ECHO* | GPIO 13          | Echo Pin for Ultrasonic Sensor    |
| *Push Button*     | GPIO 15          | Push Button for Manual Override   |
| *Buzzer*          | GPIO 16          | Buzzer for Alert                  |

### *Project Workflow*:
1. The *ultrasonic sensor* constantly measures the distance from any object behind the vehicle.
2. If an obstacle is detected within a specified range (e.g., 5 cm), the *motors* are stopped to prevent collision.
3. The *buzzer* sounds an alert to notify the driver of the detected obstacle.
4. Pressing the *push button* overrides the obstacle detection for 1 minute, allowing the motors to run even if there is an obstacle.
5. After the obstacle is resolved, the *buzzer* turns off for 1 minute as a safety feature.

### *How to Use*:
1. *Upload the Code*: Upload the code to the ESP32 using the Arduino IDE or PlatformIO.
2. *Connect the Components*: Wire the ultrasonic sensor, motors, motor driver, push button, and buzzer to the ESP32 according to the pin configuration table.
3. *Power On*: Supply power to the ESP32 and other components.
4. *Test the System*: Move objects behind the vehicle and observe how the system reacts, including stopping the motors and activating the buzzer.

### *License*:
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
