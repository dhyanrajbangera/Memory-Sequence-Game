
# Firmware

This directory contains the Arduino firmware that controls the Memory Sequence Game.

## File

| File | Description |
|---|---|
| `memorygame.ino` | Main Arduino sketch: initializes the hardware, generates the color sequence, reads player input, manages difficulty, and handles game-over behavior. |

## Firmware Responsibilities

- Configures four LED outputs and four button inputs.
- Uses Arduino internal pull-up resistors for button inputs.
- Generates a pseudo-random color sequence.
- Plays a distinct buzzer tone for each color.
- Checks player input against the generated sequence.
- Increases sequence length after each successful round.
- Gradually reduces playback timing to increase difficulty.
- Displays a game-over animation and automatically restarts the game.

## Pin Assignment

| Component | Pin | Configuration |
|---|---:|---|
| Red LED | D2 | Output |
| Red button | D3 | INPUT_PULLUP |
| Yellow LED | D4 | Output |
| Yellow button | D5 | INPUT_PULLUP |
| Green LED | D6 | Output |
| Green button | D7 | INPUT_PULLUP |
| Blue LED | D8 | Output |
| Blue button | D9 | INPUT_PULLUP |
| Buzzer | D12 | Tone output |
| Random seed input | A0 | Analog input |

## Upload Instructions

1. Install the Arduino IDE.
2. Open `memorygame.ino`.
3. Connect the Arduino-compatible board.
4. Select the correct board and port.
5. Verify the wiring.
6. Upload the sketch.
7. Open Serial Monitor at 9600 baud.

## Gameplay Timing

| Parameter | Initial value | Minimum |
|---|---:|---:|
| LED sequence on-time | 300 ms | 100 ms |
| Gap between sequence steps | 180 ms | 50 ms |
| Speed adjustment per successful round | 15 ms | — |
| Player feedback duration | 180 ms | — |

The sequence on-time and gap decrease by 15 ms after each successful round, subject to their minimum values.

## Implementation Notes

- Buttons are active-low because the sketch uses INPUT_PULLUP.
- The random sequence is initialized using randomSeed(analogRead(A0)).
- The current implementation uses delay() and blocking button-wait loops.
- The sequence arrays support up to 100 entries, with level handling preventing array overflow.

## Electrical Safety

Use current-limiting resistors with all LEDs. Check the buzzer's electrical requirements before connecting it directly to a GPIO pin. Use an appropriate driver if necessary.

See the `docs/` directory for complete hardware and assembly information.
