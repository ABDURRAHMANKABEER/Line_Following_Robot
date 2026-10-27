## Day 1: System Understanding and Simulator Investigation

### Objective
Understand the basic operation of a line-following robot and identify the roles of its sensors, controller, motor driver, and motors.

### Key Concepts Learned
- A sensor provides information about the environment; it does not independently decide how the robot should move.
- A single sensor can indicate whether the line is beneath that sensor, but multiple sensors provide more information about the line's position relative to the robot.
- The Arduino interprets sensor information and determines the appropriate steering action.
- The motor driver controls the power supplied to the motors based on the controller's commands.
- Robot movement changes subsequent sensor readings, allowing the controller to make repeated steering corrections.

### System Architecture
IR Sensors → Arduino Controller → Motor Driver → Left and Right Motors → Updated Sensor Readings

### Practical Investigation
- Opened a browser-based robotics simulator.
- Observed a line-following robot exhibiting zigzag movement.
- Identified visible sensor readings and adjustable controls.
- Recognized that the initial simulator was too advanced for the current learning stage.
- Switched to a simpler, step-by-step learning approach, beginning with the purpose of one sensor before introducing multiple sensors.

### Outcome
Established a basic understanding of the sensing, decision-making, and movement stages of a line-following robot.

### Next Step
Investigate sensor arrangements and learn how left, centre, and right sensor readings help the Arduino estimate the line's position.