## Day 2: Sensor Patterns and Interpretation

### Objective
Understand how multiple line sensors help the Arduino estimate the position of a black line relative to the robot.

### Key Concepts Learned
- A sensor provides information about the environment; the Arduino interprets the readings.
- Three sensors can be arranged as Left, Centre, and Right.
- For our simplified logical convention, `1` means black detected and `0` means black not detected.
- Sensor patterns help estimate the line's position.
- The Arduino uses sensor readings to decide how the robot should steer.
- In a differential-drive robot, changing the relative speeds of the left and right motors changes the turning direction.
- A small difference between motor speeds can produce a gentle turn, while a larger difference can produce a sharper turn.

### Sensor Pattern Examples

| Left | Centre | Right | Interpretation |
|---:|---:|---:|---|
| 0 | 1 | 0 | Line approximately centred |
| 1 | 0 | 0 | Line toward the left |
| 0 | 0 | 1 | Line toward the right |
| 0 | 0 | 0 | No sensor detects the line |
| 1 | 1 | 0 | Line detected by the left and centre sensors |
| 0 | 1 | 1 | Line detected by the centre and right sensors |

*Note: These are simplified interpretations. Actual sensor outputs and patterns depend on the sensor module, track geometry, and line width.*

### Practical Work
- Used a simple interactive simulation to change three logical sensor readings.
- Observed how different patterns changed the interpretation of the line's position.
- Discussed how sensor information could guide the robot's steering response.

### Outcome
Developed a basic understanding of multi-sensor line detection, interpreting sensor patterns, and the relationship between differential motor speeds and steering.

### Next Step
Investigate how to represent sensor readings in Arduino code and connect those readings to simple motor commands.