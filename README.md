# 🧩 Maze Solving LEGO EV3 Robot

> A software-controlled autonomous robot that navigates through a maze using sensor feedback and implements a "Left First" pathfinding algorithm to reach a color-coded goal.

---

## 📌 Project Overview

This project was developed as part of the **Design and Implementation of Software Systems** course at **Technische Universität Hamburg (TU Hamburg)**.

The system involves a **LEGO LeJOS Mindstorms EV3 robot** designed to autonomously solve a maze by navigating from any random starting point within a confined 35x35 cm² grid. The robot utilizes multiple sensors to detect obstacles, identify colors, and maintain orientation in order to reach a designated **goal wall of a specific color**.

---

## 🎯 Objective

Guide the robot from an arbitrary starting position in a maze to a **target location marked by a specific color**, using:
- Sensor input for environmental awareness
- Decision-making logic based on the "Left First" algorithm
- Precise motor control and navigation

---

## 🔧 Key Features

- Autonomous maze solving using a **"Left First" exploration strategy**
- Real-time **sensor-based navigation**:
  - **Gyroscope**: For orientation and turning accuracy
  - **Ultrasonic Sensor**: For obstacle and wall detection
  - **Color Sensor**: To identify the goal area
- Modular software architecture with clear separation of concerns
- Robust state management for decision-making and movement

---

## 🤖 Hardware Components

- **LEGO Mindstorms EV3 Kit**
- **EV3 Gyro Sensor**: For directional control and turning precision
- **EV3 Ultrasonic Sensor**: Detects walls and obstacles
- **EV3 Color Sensor**: Identifies the goal area by color
- **Two Large Motors**: Control differential drive system

---

## 🛠️ Software Architecture

The software is implemented using **LeJOS EV3 firmware** in Java and follows a **modular design pattern**, separating responsibilities into distinct components:

- **Sensor Manager**: Handles data acquisition and filtering
- **Navigation Logic**: Implements the "Left First" maze-solving algorithm
- **Motor Controller**: Manages precise movements and turns
- **State Machine**: Coordinates robot behavior across different modes (e.g., exploring, turning, stopping)

---

## 🧭 Navigation Strategy: Left First Algorithm

The robot explores the maze by prioritizing left turns when possible. It makes decisions based on sensor inputs according to the following priority list:

1. **Turn Left** if possible
2. **Go Straight** if no left turn available
3. **Turn Right** if only right is open
4. **U-turn** if completely blocked

This ensures efficient coverage and eventual arrival at the goal.

---

## 🎮 Operation Workflow

1. **Start Up**: Robot initializes sensors and motors.
2. **Search Mode**: Begins navigating the maze using the "Left First" algorithm.
3. **Wall Detection**: Uses ultrasonic sensor to avoid collisions and track walls.
4. **Goal Detection**: Scans for the target color using the color sensor.
5. **Arrival**: Upon detecting the goal color, the robot stops and signals completion.

---

## 📋 Functional Behavior Summary

| Action               | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| Power On             | Initializes all sensors and motors                                         |
| Detect Wall (Left)   | Turns left                                                                  |
| No Left Path         | Tries straight, then right                                                  |
| Dead End             | Performs U-turn                                                             |
| Goal Color Detected  | Stops and signals successful completion                                    |

---

## 🎓 Course Context

This project was completed as part of the **Design and Implementation of Software Systems** course at **Technische Universität Hamburg (TU Hamburg)**. It demonstrates:
- Object-oriented design in embedded robotics
- Sensor integration and real-time feedback
- State machine modeling
- Algorithmic problem solving in constrained environments
- Systematic software development process

---

## 🧪 Future Improvements

- Implement path optimization or mapping
- Integrate A* or Dijkstra’s algorithm for shortest path computation
- Add Bluetooth communication for remote monitoring
- Use image processing for advanced color recognition

---

## 📚 Dependencies & Tools

- **Platform**: LEGO LeJOS EV3
- **Language**: Java
- **IDE**: Eclipse 
- **Libraries**: LeJOS API
