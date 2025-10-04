# Keypad Robot Navigation Controller

This project uses an Arduino-compatible board (like an ESP32) to control a robot based on user input from a keypad.
It allows a user to program a sequence of distances and 90-degree turns. The robot then executes this path, using an MPU6050 gyroscope for accurate turning.

## Hardware Required
* ESP32 / Arduino
* 16x2 LCD Display
* 4x3 Matrix Keypad
* MPU6050 Gyroscope
* Robot chassis with an I2C motor controller (slave at address `0x04`)

## How to Use
1.  **Enter Distance:** Use the number keys to input how far the robot should move.
2.  **Enter Turn:** Press `*` to switch to angle mode. Press `1` for a 90° left turn or `2` for a 90° right turn.
3.  **Build Path:** Press `*` to toggle between distance and angle input to add more steps.
4.  **Start:** Press `#` to run the programmed sequence.

## Dependencies

* `<LiquidCrystal.h>`
* `<Keypad.h>`
* `<Wire.h>`
* `<MPU6050_tockn.h>`

## Important Note

The code sends movement commands over I2C to a slave motor controller.
