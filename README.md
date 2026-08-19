# 🤖 Autonomous LEGO MINDSTORMS EV3 Robot

An autonomous LEGO MINDSTORMS EV3 vehicle designed, built, and programmed with MATLAB to navigate a maze, respond to environmental markers, and safely transport a model wheelchair passenger from pickup to drop-off.

**Platform:** LEGO MINDSTORMS EV3  
**Programming Language:** MATLAB  
**Team Size:** 4

---

## 📸 Project Preview

<!-- IMAGE 1: Robot navigating the maze near the yellow zone -->
![LEGO EV3 Robot Navigating Maze](images/robot-maze.jpg)

*Autonomous LEGO MINDSTORMS EV3 robot navigating the physical maze course during testing.*

---

## 🎯 Project Overview

This project challenged our four-person team to design, build, program, and test an autonomous vehicle using the LEGO MINDSTORMS EV3 platform.

The goal was to create a robot capable of navigating different maze configurations without direct human control while completing a passenger transportation mission.

The robot needed to:

1. Begin at the designated starting area
2. Autonomously navigate the maze
3. Stop when encountering designated stop markers
4. Reach the passenger pickup point
5. Pick up a model representing a person in a wheelchair
6. Safely transport the passenger through the maze
7. Reach the designated drop-off point
8. Unload the passenger
9. Complete the course

In addition to completing the route, the vehicle needed to remain stable, avoid becoming trapped in navigation loops, and transport the passenger safely.

---

## ⚙️ Robot Design

<!-- IMAGE 2: Clean side view showing EV3 brick, sensors, wheels, and mechanisms -->
![LEGO EV3 Robot Hardware](images/robot-hardware.jpg)

*Side view of the completed vehicle showing the EV3 hardware, sensors, wheels, chassis, and custom mechanisms.*

Our team collaboratively designed and constructed the vehicle using LEGO components and the MINDSTORMS EV3 platform.

The robot incorporated:

- LEGO MINDSTORMS EV3 programmable brick
- Electric drive motors
- Color sensing
- Touch sensing
- Distance/proximity sensing
- Custom LEGO chassis
- Mechanical passenger handling system

The physical design had to support both autonomous navigation and passenger transportation while remaining stable during movement and turns.

---

## 🧠 Autonomous Navigation

The robot used multiple sensor inputs to make decisions as it traveled through the maze.

The navigation system was designed around several basic behaviors:

- **Clear path →** Continue forward
- **Front obstacle/contact →** Turn right
- **Opening detected on the left →** Turn left
- **Course marker detected →** Perform the appropriate programmed action

This allowed the vehicle to react to its surroundings instead of relying entirely on a predetermined sequence of movements.

### Navigation Concept

```text
                Read Sensors
                     │
                     ▼
             Check Course Marker
                     │
                     ▼
             Check Surroundings
              /      |       \
         Wall Ahead  Left Open  Clear
              │          │        │
          Turn Right   Turn Left  Forward
              \          |        /
                     ▼
                   Repeat
```

The robot continuously repeated this decision process as it progressed through the course.

---

## 🚦 Course Markers & Mission

Different colored areas of the course represented important locations or instructions within the autonomous mission.

| Color | Purpose |
| --- | --- |
| 🟨 **Yellow** | Starting / ending area |
| 🟦 **Blue** | Passenger pickup point |
| 🟩 **Green** | Passenger drop-off point |
| 🟥 **Red** | Stop marker |

The robot's color sensing allowed it to recognize these areas and perform the appropriate action as it progressed through the maze.

### Mission Sequence

```text
🟨 START
    │
    ▼
Navigate Maze
    │
    ├──── 🟥 STOP MARKER
    │         │
    │      Stop briefly
    │         │
    ▼         ▼
🟦 PASSENGER PICKUP
    │
    ├──── Load Passenger
    │
    ▼
Continue Navigation
    │
    ├──── 🟥 STOP MARKER
    │         │
    │      Stop briefly
    │         │
    ▼         ▼
🟩 PASSENGER DROP-OFF
    │
    ├──── Unload Passenger
    │
    ▼
Continue Navigation
    │
    ▼
🟨 FINISH
```

---

## ♿ Passenger Transportation

<!-- IMAGE 3: Robot positioned on the blue passenger pickup zone -->
![Passenger Pickup](images/passenger-pickup.jpg)

*Robot positioned at the blue passenger pickup area during maze testing.*

A major component of the project was transporting a cardboard model representing a person using a wheelchair.

The vehicle incorporated a mechanical system that allowed it to interact with the passenger at designated locations.

The complete transportation mission required the robot to autonomously navigate to the pickup area, secure the passenger, transport the passenger through the maze, reach the drop-off area, and safely release the passenger.

Passenger safety also influenced the physical design. The robot needed to avoid tipping over or making movements that could cause the passenger to fall during transportation.

---

## 🧪 Engineering Requirements

Successful completion required more than simply reaching the end of the maze.

The vehicle needed to:

- Navigate different maze configurations autonomously
- Detect walls and available paths
- Respond correctly to sensor input
- Recognize designated course markers
- Stop at required stop locations
- Reach the passenger pickup point
- Successfully load the passenger
- Transport the passenger through the maze
- Reach the designated drop-off point
- Safely unload the passenger
- Avoid becoming trapped in repeating navigation loops
- Remain stable and avoid tipping over
- Complete the mission without direct human control

---

## 🛠️ Technologies & Concepts

**Hardware & Software**
- MATLAB
- LEGO MINDSTORMS EV3
- EV3 Sensors & Motors

**Engineering Concepts**
- Autonomous Robotics
- Sensor Integration
- Motor Control
- Conditional Logic
- Obstacle Detection
- Hardware & Software Integration
- Mechanical Design
- Testing & Iteration

---

## 👥 Team Collaboration

<!-- IMAGE 4: Team photo holding the completed robot -->
![Project Team](images/team.jpg)

*Project team with the completed LEGO MINDSTORMS EV3 robot.*

This project was completed as part of a four-person engineering team.

We collaborated on the robot's physical design, programming approach, sensor integration, navigation strategy, testing, troubleshooting, and iterative improvements.

Developing a successful solution required coordinating the software and mechanical components of the vehicle while repeatedly testing its performance on the physical course.

---

## 🧪 Testing & Iteration

The robot was tested repeatedly throughout development to identify problems and improve its autonomous behavior.

Testing focused on areas such as:

- Sensor response
- Obstacle detection
- Turning behavior
- Color recognition
- Maze navigation
- Passenger pickup and drop-off
- Vehicle stability
- Avoiding repeated navigation loops
- Overall mission completion

Each test provided feedback that could be used to adjust the physical design or programming logic before testing again.

---

## 💡 What I Learned

This project provided hands-on experience combining software, robotics, and mechanical design to solve a real engineering challenge.

Key takeaways included:

- Programming robotic hardware using MATLAB
- Integrating multiple sensors into autonomous decision-making
- Translating sensor readings into physical motor actions
- Developing conditional navigation logic
- Combining software with physical hardware
- Troubleshooting autonomous system behavior
- Testing and iteratively improving a physical system
- Designing around stability and passenger safety
- Collaborating within an engineering team

---

## 📁 Repository Structure

```text
autonomous-lego-ev3-robot/
│
├── README.md
│
└── images/
    ├── robot-maze.jpg
    ├── robot-hardware.jpg
    ├── passenger-pickup.jpg
    └── team.jpg
```

---

## 📝 Project Note

This repository documents the design, functionality, and engineering process of the original LEGO MINDSTORMS EV3 project.

The original MATLAB source code is no longer available. The system behavior and navigation concepts documented here are based on the original project's design and functionality rather than a reproduction of the original source code.
