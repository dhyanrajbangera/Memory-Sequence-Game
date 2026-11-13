
# Build Guide

This guide describes the assembly and upload workflow for the Memory Sequence Game.

## 1. Prepare the Components

Gather the components listed in HARDWARE.md. Check LED polarity and confirm that the push buttons are normally-open momentary switches.

## 2. Assemble the Circuit

Use PINOUT.md to connect each LED, button, and buzzer.

Important:
- Each LED must have a suitable current-limiting resistor.
- Buttons use Arduino internal pull-up resistors.
- Connect one side of each button to its assigned input pin and the other side to GND.
- Confirm the buzzer's voltage and current requirements.
- Keep all circuit grounds common.

Check the wiring before powering the circuit.

## 3. Upload the Firmware

1. Install Arduino IDE.
2. Open `firmware/memorygame.ino`.
3. Connect the board over USB.
4. Choose the correct board and port.
5. Upload the sketch.
6. Open Serial Monitor at 9600 baud.

## 4. Test the Game

1. Confirm that each LED illuminates.
2. Confirm that each button produces matching color and tone feedback.
3. Watch the sequence and repeat it.
4. Test an incorrect input.
5. Confirm that the game restarts automatically.

## 5. Print and Fit the Enclosure

Inspect:
- Model dimensions and scale.
- Button and LED alignment.
- Board and wiring clearance.
- USB access.
- Buzzer opening.
- Lid-to-base fit.

Print a fit-check prototype before final production.

## Troubleshooting

| Symptom | Checks |
|---|---|
| Board not detected | USB cable, board selection, driver, port |
| LED does not illuminate | Polarity, resistor, wiring, pin |
| Button always active | Button wiring and INPUT_PULLUP |
| No buzzer sound | Buzzer type, pin D12, wiring |
| Sequence seems inconsistent | Wiring and A0 input |
| Enclosure does not fit | STL scale and component dimensions |
