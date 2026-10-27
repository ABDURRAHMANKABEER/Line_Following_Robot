# Project 4: Arduino Line-Following Robot

## 1. Project Overview

The Line-Following Robot is an autonomous robotic system that detects a line on a surface and controls its movement to follow that line without continuous human intervention.

The robot uses infrared (IR) reflectance sensors to detect the line, an Arduino microcontroller to process sensor readings and make steering decisions, and a motor driver to control two DC motors.

This project builds on previous work with Arduino, sensor inputs, motor control, PWM, and basic control logic. It introduces more advanced practical concepts in robotics, multi-sensor interpretation, differential drive, steering algorithms, calibration, and system debugging.

## 2. Project Objectives

The objectives of this project are to:

- Understand how IR reflectance sensors detect lines.
- Interpret readings from multiple sensors to estimate the line's position.
- Control two DC motors independently using a motor driver.
- Understand differential-drive motion and how wheel speeds affect robot movement.
- Develop steering logic that responds to sensor readings.
- Implement and investigate proportional steering.
- Understand calibration, oscillation, and line-loss recovery.
- Practise systematic testing and debugging.
- Document the design, implementation, experiments, and results using Git and GitHub.

## 3. System Architecture

The robot follows this basic signal flow:

```text
       Track / Surface
              |
              v
      IR Reflectance Sensors
              |
              v
       Arduino Controller
              |
              v
       Steering Algorithm
              |
              v
         Motor Driver
          /        \
         v          v
    Left Motor   Right Motor
          \        /
           v      v
         Robot Motion
              |
              v
       Updated Sensor Readings
```

The robot's movement changes the position of its sensors relative to the line. The resulting sensor readings influence subsequent steering decisions, forming a feedback loop.

## 4. Main Components

The intended system consists of:

- Arduino-compatible microcontroller.
- IR reflectance sensor or sensor array.
- Two DC motors.
- Dual-motor driver.
- Robot chassis and wheels, where supported.
- Suitable power supply for the controller and motors.
- Connecting wires and connectors.

The exact components and simulation substitutes will be confirmed during the design stage.

## 5. Development Environment

- **Programming:** Arduino C/C++.
- **Development and documentation:** Visual Studio Code.
- **Version control:** Git and GitHub.
- **Initial testing:** Circuit and component simulation where supported.
- **Robot movement visualization:** To be selected when required by the project.
- **Circuit design:** To be documented as the hardware design develops.

The initial implementation will be simulation-based. Physical hardware testing will be considered separately when the necessary components are available.

## 6. Planned Development Stages

The project will be developed incrementally over ten days.

| Day | Focus |
|---|---|
| 1 | Project setup and IR sensor investigation |
| 2 | Multiple sensor inputs and calibration |
| 3 | Two-motor control and differential drive |
| 4 | Motor-control functions and movement experiments |
| 5 | Sensor interpretation and steering algorithm |
| 6 | Integration of the first line-following system |
| 7 | Calibration and line-loss recovery |
| 8 | Introduction to proportional steering |
| 9 | Performance tuning and systematic debugging |
| 10 | Final testing, evaluation, and documentation |

The schedule may be adjusted when experiments reveal an important concept that needs further investigation.

## 7. Key Engineering Concepts

### Electronics
- IR reflectance sensors.
- Digital and analog sensor outputs.
- Motor drivers and independent motor control.
- PWM-based speed control.
- Power supply requirements and electrical noise.
- Sensor placement and mechanical alignment.

### Embedded Programming
- Reading multiple inputs.
- Variables, conditional logic, and functions.
- Arrays and sensor-state representation.
- PWM and motor-direction commands.
- Serial debugging and code organization.

### Control Engineering
- Feedback systems.
- Sensor-based steering decisions.
- Differential-drive motion.
- Line-position error.
- Proportional control.
- Calibration, oscillation, and recovery behaviour.

### Practical Engineering
- System decomposition and integration.
- Testing individual subsystems.
- Developing repeatable test cases.
- Identifying hardware, software, and system-level faults.
- Recording observations and justifying design changes.

## 8. Testing and Evaluation

The robot will be evaluated through progressively more challenging tests:

1. Correct interpretation of individual sensor readings.
2. Correct interpretation of combined sensor patterns.
3. Independent control of the left and right motors.
4. Correct steering responses to different sensor patterns.
5. Basic line following on a straight path.
6. Response to curves and sharper turns.
7. Behaviour when the line is lost.
8. Comparison of basic steering and proportional steering.
9. Repeatability and performance under different test conditions.

Simulation results will be distinguished from behaviours that require physical hardware validation.

## 9. Daily Documentation

Each day's work will record:

- Objective.
- Concepts investigated.
- Circuit or system changes.
- Code written and tested.
- Experiments performed.
- Expected versus observed behaviour.
- Problems encountered and how they were investigated.
- Lessons learned.
- Remaining tasks and proposed improvements.

Daily work will be committed to Git using meaningful commit messages.

## 10. Expected Outcome

By the end of the project, the goal is to have a working simulated line-following robot whose sensor interpretation, motor commands, and steering behaviour can be explained and tested.

The project should also provide practical experience in integrating electronics, embedded software, and control logic into a single autonomous system.

The emphasis is not merely on making the robot follow a line, but on understanding why it works, identifying why it fails, and making informed engineering improvements.

## 11. Project Status

**Status:** Planned — initial setup and investigation pending.

**Current phase:** Project documentation and system understanding.

**Next milestone:** Investigate IR sensor behaviour and establish the robot's initial system requirements before implementation.