# 4-Servo Motor Control – Sweep then Hold

## Overview
This project programs **4 servo motors** using an Arduino (simulated on Tinkercad) to perform the following sequence:

1. Run a **Sweep** motion (0° → 180° → 0°) on all 4 servos simultaneously for **2 seconds**.
2. After the 2 seconds elapse, all 4 servos **hold at 90°**.

## Components Used
- Arduino Uno
- 4x Servo Motors
- Jumper wires
- Simulated on [Tinkercad Circuits](https://www.tinkercad.com/circuits)

## Circuit Connections

| Servo   | Signal Pin | Power (V+) | Ground (GND) |
|---------|-----------|------------|---------------|
| Servo 1 | Pin 3     | 5V         | GND           |
| Servo 2 | Pin 5     | 5V         | GND           |
| Servo 3 | Pin 6     | 5V         | GND           |
| Servo 4 | Pin 9     | 5V         | GND           |

> Note: Pins 3, 5, 6, and 9 support PWM (marked with `~`), which is required for servo control.

## How It Works
- The `Servo.h` library is used to control all 4 servos.
- In `setup()`, a `millis()`-based timer runs a sweep loop (0°→180°→0°) on all servos for exactly 2 seconds.
- Once the 2-second window ends, all servos are explicitly set to 90° and remain there.
- The `loop()` function is left empty since no further action is needed after the servos are set to hold position.

## Code
See [`four_servos_sweep_then_hold.ino`]([./four_servos_sweep_then_hold.ino](https://www.tinkercad.com/things/atn348yqXrv/editel?returnTo=%2Fdashboard%2Fdesigns%2Fcircuits&sharecode=0eKTZfvaXV79jWiwMnYhrZvpkSt6D8XffJaArWgfvI0)) for the full Arduino sketch.

## How to Run (Tinkercad)
1. Create a new circuit in Tinkercad and add an Arduino Uno + 4 servo motors.
2. Wire each servo's signal pin to pins 3, 5, 6, and 9 respectively (see table above).
3. Open the **Code** editor, switch to **Text** mode, and paste the sketch.
4. Click **Start Simulation** to observe the servos sweep for 2 seconds, then hold at 90°.

## Author

Hind Almutairi

Computer Science Student

