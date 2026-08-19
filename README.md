# 🤖 Autonomous LEGO MINDSTORMS EV3 Robot

An autonomous LEGO MINDSTORMS EV3 vehicle designed and programmed with MATLAB to navigate a maze, respond to environmental conditions, and safely transport a model wheelchair passenger.

**Platform:** LEGO MINDSTORMS EV3  
**Programming Language:** MATLAB  
**Team Size:** 4

---

## 📸 Project Preview

<!-- Replace with a photo of the completed robot -->
![Completed LEGO EV3 Robot](images/robot-overview.jpg)

---

## 🎯 Project Overview

This project challenged our four-person team to design, build, program, and test an autonomous LEGO MINDSTORMS EV3 vehicle capable of navigating different maze configurations.

The robot needed to autonomously navigate the maze, respond to colored markers and obstacles, pick up a model wheelchair passenger using a mechanical lift, and safely transport the passenger to the designated drop-off point.

Successful completion required the robot to remain stable, avoid navigation loops, correctly interpret sensor input, and complete the course without human assistance.

---

## ⚙️ Robot Design

Our team collaboratively designed and constructed the vehicle using LEGO components and the MINDSTORMS EV3 platform.

The robot incorporated:

- EV3 programmable brick
- Drive motors
- Color sensor
- Touch sensor
- Distance/proximity sensor
- Mechanical passenger lift
- Custom LEGO chassis

<!-- Replace with a side or top view showing the robot's components -->
![Robot Design](images/robot-design.jpg)

---

## 🧠 Autonomous Behavior

The robot used sensor input to determine how it should respond to its environment.

| Input | Robot Response |
| --- | --- |
| 🔴 Red detected | Stop temporarily |
| 🟡 Yellow detected | Reduce speed |
| 🟢 Green detected | Activate passenger lift |
| Front touch sensor triggered | Turn right |
| Opening detected on left | Turn left |
| Clear path | Continue forward |

This allowed the vehicle to continuously evaluate its surroundings and make navigation decisions without direct human control.

---

## 🧭 Navigation Logic

The general autonomous navigation process followed this behavior:

```text
             Read Sensors
                  │
                  ▼
          Check Color Sensor
          /       |        \
       RED      YELLOW     GREEN
        │          │          │
       Stop     Slow Down   Lift Action
        \          |          /
                  ▼
          Check Navigation
          /       |        \
   Wall Ahead  Left Open   Clear
       │           │         │
   Turn Right   Turn Left   Forward
        \          |         /
                  ▼
                Repeat
```

The combination of touch, distance, and color sensing allowed the robot to react dynamically as it moved through the maze.

---

## ♿ Passenger System

An important requirement was safely transporting a cardboard model representing a person using a wheelchair.

The robot incorporated a mechanical lift that allowed it to interact with the passenger at designated locations.

The autonomous mission involved:

1. Navigate through the maze
2. Reach the passenger pickup point
3. Detect the appropriate marker
4. Activate the lift
5. Secure the passenger
6. Continue navigating
7. Reach the drop-off point
8. Safely unload the passenger

<!-- Replace with a photo of the lift/passenger system -->
![Passenger Lift System](images/passenger-lift.jpg)

---

## 🧪 Design Requirements

The final robot needed to:

- Navigate different maze configurations autonomously
- Respond correctly to sensor input
- Detect walls and available paths
- React appropriately to colored markers
- Pick up and transport the passenger
- Successfully reach the drop-off point
- Avoid becoming trapped in repeating navigation loops
- Remain stable and avoid tipping over
- Transport the passenger without causing damage

---

## 🛠️ Technologies & Concepts

- MATLAB
- LEGO MINDSTORMS EV3
- Autonomous Robotics
- Sensor Integration
- Motor Control
- Conditional Logic
- Obstacle Detection
- Mechanical Design
- Hardware & Software Integration
- Testing & Iteration

---

## 👥 Team Collaboration

This project was completed by a team of four.

Our team collaborated on the robot's physical design, programming approach, sensor integration, testing, troubleshooting, and iterative improvements needed to successfully complete the autonomous maze challenge.

---

## 📸 Testing & Final Result

The robot was repeatedly tested and adjusted to improve navigation accuracy, stability, sensor responses, and passenger transportation.

<!-- Replace with a photo of the robot navigating the maze -->
![Maze Testing](images/maze-testing.jpg)

<!-- Replace with a photo of the completed course or passenger transport -->
![Final Demonstration](images/final-demonstration.jpg)

---

## 💡 What I Learned

This project provided hands-on experience combining programming with physical hardware to solve an engineering problem.

Key takeaways included:

- Programming robotic hardware with MATLAB
- Using multiple sensors for autonomous decision-making
- Translating sensor readings into motor actions
- Developing conditional navigation logic
- Troubleshooting interactions between software and hardware
- Improving a physical system through repeated testing
- Designing around stability and safety requirements
- Collaborating within an engineering team

---

## 📝 Project Note

This repository documents the design, functionality, and engineering process of the original project. The original MATLAB source code is no longer available, so the logic shown here represents the system's behavior rather than a reproduction of the original implementation.
