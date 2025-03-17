# Automatic Temperature and Water Controlling System

This project uses Arduino to automatically control temperature and water flow. The system monitors ambient temperature and activates a servo motor or valve to regulate water flow when the temperature exceeds a set threshold.

## Features
- Monitors temperature with a **TMP36 sensor**.
- Controls water flow with a **servo motor** or **electronic valve**.
- Displays temperature and water flow status on **two I2C LCD screens**.
- **LED indicator** for cooling system status.

## Components
- **Arduino Uno** (or compatible)
- **TMP36 Temperature Sensor**
- **16x2 I2C LCD Display** (2 units)
- **Servo Motor (SG90)** or **Electronic Valve**
- **LED**

## Feedback Loop
- **Sensing**: Collects temperature data.
- **Processing**: Analyzes data with control algorithms.
- **Actuation**: Adjusts water flow based on the temperature.

## Control Logic
- **Temperature increases**: Cooling system turns ON.
- **Temperature decreases**: Cooling system turns OFF.

## Applications
- **Greenhouses**: Optimizes temperature for plant growth.
- **Industrial Equipment**: Manages cooling in machinery.
- **Home Automation**: Regulates temperature for comfort.

## Advantages
- Reduces manual intervention.
- Ensures optimal temperature and water levels.
- Efficient and automated solution for various applications.

## Conclusion
This system provides automated temperature and water control, making it ideal for industrial, agricultural, and home applications.
