# Memory-Sequence-Game
An Arduino-based electronic memory game featuring four-color LED sequences, push-button interaction, buzzer feedback, progressive difficulty, and a custom 3D-printed enclosure.
Memory Sequence Game

An Arduino-based interactive memory game that challenges players to remember and reproduce increasingly complex sequences of LED patterns using physical push buttons.

Project Overview

The Memory Sequence Game is an embedded electronics project built using an Arduino microcontroller. It generates randomized LED sequences that players must memorize and repeat using corresponding push buttons.

With every successful round, the sequence becomes longer and the game progressively more challenging. The project combines embedded programming, electronic hardware, interactive design, and custom 3D-printed enclosure components.

Key Features

- Randomized Sequences: Generates unpredictable LED patterns.
- Progressive Difficulty: Sequence length increases after each successful round.
- Four-Button Input System: Players reproduce the sequence using physical buttons.
- LED Visual Feedback: Four LEDs communicate the generated sequence.
- Buzzer Feedback: Audio feedback enhances the gameplay experience.
- Custom 3D-Printed Enclosure: Includes separately designed base and lid STL models.
- Arduino-Based Control: Game logic is implemented in Arduino C/C++.

Hardware Components

Component| Quantity
Arduino-compatible board| 1
LEDs| 4
Push buttons| 4
Current-limiting resistors| 4
Buzzer| 1
Connecting wires| As required
Breadboard or custom PCB| 1
3D-printed enclosure| 1 set

Pin Configuration

Component| Arduino Pin
Red LED| D2
Red Button| D3
Yellow LED| D4
Yellow Button| D5
Green LED| D6
Green Button| D7
Blue LED| D8
Blue Button| D9
Buzzer| D12
Random Seed Input| A0

Note: The push buttons use the Arduino "INPUT_PULLUP" configuration, so button presses are detected as LOW signals. Confirm the wiring and pin assignments against the actual hardware before powering the circuit.

Repository Structure

Memory-Sequence-Game/
│
├── firmware/
│   ├── memorygame.ino
│   └── README.md
│
├── 3d-models/
│   ├── memory-game-base.stl
│   ├── memory-game-lid.stl
│   └── README.md
│
├── docs/
│   ├── BUILD_GUIDE.md
│   ├── HARDWARE.md
│   ├── PINOUT.md
│   └── README.md
│
├── images/
│   └── README.md
│
├── .github/
│   └── ISSUE_TEMPLATE/
│       └── bug_report.md
│
├── PROJECT_INFO.md
├── CONTRIBUTING.md
├── LICENSE
└── README.md

How the Game Works

1. The Arduino generates a random sequence of LED signals.
2. The LEDs illuminate one after another to display the sequence.
3. The player memorizes the pattern.
4. The player presses the corresponding buttons in the same order.
5. If the input is correct, the player advances to the next round.
6. The sequence becomes longer as the game progresses.
7. An incorrect input ends the current attempt.

Firmware Setup

1. Download or clone this repository.
2. Open the "firmware/memorygame.ino" file in the Arduino IDE.
3. Connect the Arduino board to your computer.
4. Select the correct board and COM/serial port.
5. Verify the pin connections.
6. Upload the sketch to the board.
7. Power the circuit and start playing.

3D-Printed Enclosure

The repository includes two STL files for the physical enclosure:

- "memory-game-base.stl" – Main enclosure base.
- "memory-game-lid.stl" – Top cover.

The models can be opened in a slicer such as Ultimaker Cura or PrusaSlicer and prepared for 3D printing.

Before printing, verify the model dimensions, component clearances, button openings, and board mounting positions.

Documentation

Additional technical documentation is available in the "docs/" directory:

- BUILD_GUIDE.md – Assembly and setup instructions.
- HARDWARE.md – Hardware components and electrical considerations.
- PINOUT.md – Arduino pin assignments.
- PROJECT_INFO.md – Additional project information.

Project Applications

This project demonstrates practical experience in:

- Embedded systems development
- Arduino programming
- Digital input and output control
- Basic electronics and circuit integration
- Random sequence generation
- Hardware prototyping
- 3D modelling and enclosure design
- Interactive system development

Future Improvements

- Add an OLED display for score and game status.
- Introduce multiple difficulty modes.
- Add a high-score tracking system.
- Implement non-blocking timing for improved responsiveness.
- Design a custom PCB for a more compact build.

Contributing

Contributions, suggestions, and improvements are welcome. Please read "CONTRIBUTING.md" before submitting changes.

License

This project is licensed under the MIT License. See the "LICENSE" file for details.

---

Developed as an embedded systems and hardware prototyping project.
