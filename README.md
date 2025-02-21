# WaterLevelDetector
# Water Level Meter with Ultrasonic Sensor and LCD Display

This project uses an ultrasonic sensor to measure the water level in a tank and displays the results on an I2C LCD screen.

## Components
- Arduino Uno (or compatible microcontroller)
- Ultrasonic Sensor (HC-SR04)
- I2C LCD Display (16x2)
- Jumper wires
- Breadboard
  
![waterlevel1](https://github.com/user-attachments/assets/457a41df-8af7-408f-9c16-acb77887c881)


## Connections
### Ultrasonic Sensor:
- VCC → 5V on Arduino
- GND → GND on Arduino
- Trig → Digital Pin 8 on Arduino
- Echo → Digital Pin 9 on Arduino

### I2C LCD:
- VCC → 5V on Arduino
- GND → GND on Arduino
- SDA → A4 on Arduino (or SDA pin)
- SCL → A5 on Arduino (or SCL pin)

## Setup Instructions
1. Connect the components as per the wiring diagram.
2. Upload the provided code to your Arduino.
3. Ensure the I2C address of the LCD is correct (0x27 or 0x3F).
4. Place the ultrasonic sensor at the top of the tank, facing downward.

## Code Overview
- *LiquidCrystal_I2C Library:* Used to control the I2C LCD.
- *Ultrasonic Sensor:* Measures the distance to the water surface.
- *Tank Dimensions:* Configured in the code (tankHeight, tankLength, tankBreadth).
- *Water Level Calculation:* Converts the ultrasonic sensor reading into water level percentage, height, and volume.
- *LCD Display:* Shows the water level percentage, volume, and a progress bar.


![Waterlevel2](https://github.com/user-attachments/assets/290c3752-c21a-4423-a35a-2fa003edae64)


## Features
- *Real-Time Water Level Measurement:* Continuously measures and updates the water level.
- *Error Handling:* Displays an error message if the ultrasonic sensor fails to detect a response.
- *Progress Bar:* Visual representation of the water level on the LCD.
- *Customizable Tank Dimensions:* Adjust the tank dimensions in the code to match your setup.

## Customization
- *Tank Dimensions:* Update tankHeight, tankLength, and tankBreadth in the code to match your tank's dimensions.
- *Sensor Calibration:* Adjust tankEmptyDepth and tankFullDepth to calibrate the sensor readings for your specific setup.
- *I2C Address:* If the LCD doesn't work, try changing the I2C address to 0x3F.

## Acknowledgments
- *LiquidCrystal_I2C Library:* For simplifying I2C LCD control.
- *Arduino Community:* For providing resources and inspiration.

---
