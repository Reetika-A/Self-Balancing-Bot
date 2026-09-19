# Self-Balancing-Bot
A two-wheeled self-balancing robot using Arduino UNO, MPU6050 and PID control.
# Self-Balancing Robot

## Overview

A self-balancing robot is a two-wheeled robotic system based on the **inverted pendulum principle**. Since the robot's center of mass is above the wheel axis, it is naturally unstable and requires continuous feedback and motor correction to remain upright.

This project uses an **Arduino UNO**, **MPU6050 IMU**, **L298D motor driver**, and **DC motors** to implement a real-time balancing system.

## Components

- Arduino UNO
- MPU6050 IMU sensor
- L298D motor driver
- 2 × 12V DC motors
- 12V 3000mAh battery
- Wheels and mechanical chassis
- Connecting wires and mounting hardware

## Working Principle

The MPU6050 combines an accelerometer and gyroscope to measure the robot's orientation and detect changes in its tilt.

The Arduino UNO continuously receives sensor data and calculates the error between the current tilt angle and the desired upright position. A **PID (Proportional-Integral-Derivative) control algorithm** is used to determine the required motor correction.

When the robot tilts forward or backward, the Arduino sends appropriate control signals to the L298D motor driver. The motor driver then changes the speed and direction of the DC motors, moving the wheels to counteract the tilt and restore the robot to an upright position.

The process is continuously repeated, forming a **closed-loop feedback control system**.

## Control System

The PID controller consists of three components:

- **Proportional (P):** Provides correction based on the current tilt error.
- **Integral (I):** Accounts for accumulated error over time.
- **Derivative (D):** Responds to the rate at which the error is changing.

The combined PID output determines the direction and magnitude of motor correction.

## Challenges

- Maintaining stability during continuous movement
- Accurate sensor calibration and orientation measurement
- Tuning PID parameters
- Handling motor response and variations
- Maintaining stable operation under external disturbances

## Applications

- Robotics and embedded-systems education
- Control-system experimentation
- Autonomous robotic platforms
- Sensor-fusion research
- Demonstration of real-time feedback control

## Future Scope

The project can be further improved by implementing sensor-fusion techniques, wireless control, obstacle detection, autonomous navigation, and more advanced control algorithms.

## Technologies Used

**Hardware:** Arduino UNO, MPU6050, L298D, DC Motors

**Concepts:** PID Control, Inverted Pendulum, Closed-Loop Control, Sensor Integration

**Programming:** Embedded C/C++

## Project Structure

```text
Self-Balancing-Robot/
│
├── Arduino_Code/
│   └── Self_Balancing_Robot.ino
│
├── Images/
│   └── project images
│
└── README.md
```