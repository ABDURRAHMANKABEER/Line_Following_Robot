## Day 2: Sensor Patterns, Interpretation and Proportional Steering

### Objective
Understand how multiple line sensors estimate the position of a black line relative to a robot and how sensor information can influence motor speed and steering decisions.

### 1. Sensor Patterns and Interpretation

Investigated how three sensors arranged as Left, Centre and Right can provide information about the position of a black line.

Using the simplified logical convention:

- `1` = Black detected.
- `0` = Black not detected.

| Left | Centre | Right | Interpretation |
|---:|---:|---:|---|
| 0 | 1 | 0 | Line approximately centred |
| 1 | 0 | 0 | Line toward the left |
| 0 | 0 | 1 | Line toward the right |
| 0 | 0 | 0 | No sensor detects the line |
| 1 | 1 | 0 | Line detected by left and centre sensors |
| 0 | 1 | 1 | Line detected by centre and right sensors |

### 2. Differential Drive and Steering

Learned how changing the relative speeds of two independently controlled motors affects the robot's direction.

- Equal motor speeds produce approximately straight movement.
- Right motor faster than left motor produces a leftward turn.
- Left motor faster than right motor produces a rightward turn.

A small difference in motor speeds produces a gentler correction, while a larger difference produces a stronger correction.

### 3. Practical Investigation Using Mokxi

Explored Mokxi's Arduino line-following simulation to understand the relationship between line displacement and motor speed commands.

Moved the line-position slider and observed how the left and right motor commands changed.

#### Observed Results

| Line Position | Left Motor | Right Motor |
|---:|---:|---:|
| -15 mm | 75 | 165 |
| -7 mm | 99 | 141 |
| 0 mm | 120 | 120 |
| +7 mm | 141 | 99 |
| +15 mm | 165 | 75 |

#### Observations

- At 0 mm, both motors receive equal speed commands.
- At -7 mm and -15 mm, the right motor receives a higher command than the left motor.
- At +7 mm and +15 mm, the left motor receives a higher command than the right motor.
- Increasing line displacement produces a greater difference between the motor commands.

### 4. Introduction to Proportional Control

Discovered the basic principle of proportional control through the line-following simulation.

The controller adjusts the motor speed difference according to the displacement of the line from the robot's centre.

The fundamental relationship is:

\[
u = K_p e
\]

Where:

- \(u\) represents the control correction.
- \(K_p\) represents the proportional gain.
- \(e\) represents the line-position error.

This provided a practical introduction to a control concept previously encountered in Control Systems coursework.

### 5. Outcome

Developed an understanding of:

- Multi-sensor line detection.
- Interpreting sensor patterns.
- Differential-drive steering.
- Motor speed adjustment.
- The basic principle of proportional control.

### Next Step

Investigate the internal operation of the Mokxi line-following example, understand how line-position information is obtained, and begin developing an independent Arduino-based line-following controller.