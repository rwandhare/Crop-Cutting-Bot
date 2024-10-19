# Crop Cutting Bot

This project presents the development of an automated Crop Cutting Bot designed to assist in agricultural tasks by cutting crops efficiently. It is powered by two separate battery systems, one for bot locomotion and the other for operating the crop cutting blade. The bot is controlled remotely using a Flysky FS-i6 transmitter and receiver setup.

## Table of Contents
- [Overview](#overview)
- [Components](#components)
- [Working](#working)
- [Real-Time Application](#real-time-application)
- [Conclusion](#conclusion)
- [How to Build](#how-to-build)
- [License](#license)

## Overview

The Crop Cutting Bot is designed to automate crop cutting tasks and reduce manual labor in agriculture. By utilizing separate battery systems for locomotion and blade operation, it can efficiently move through fields and cut crops with precision. This project demonstrates the potential for agricultural automation by using components like an Arduino Uno R3, motor driver, and e-bike brush motor.

## Components

1. Flysky FS-i6: Remote control system for sending commands.
2. Jonson Gear Motor: Used for driving the wheels and moving the bot.
3. Motor Driver L298: Controls the motors for bot movement.
4. E-Bike Brush Motor: Powers the crop cutting blade.
5. Motor Mount Pair: Provides support for mounting motors.
6. Crop Cutting Blade: Responsible for cutting crops.
7. Lithium-Ion Batteries: Power the locomotion and blade systems.
8. Gear Ring and Chain: Transmits power to the wheels for locomotion.
9. Wheels: Allows movement of the bot.
10. Buck Converter: Converts voltage from 12V-20A to 12V-10A.

## Working

The bot operates using two separate power systems:
- Battery 1 powers the locomotion, Arduino, motor driver, and Flysky FS-i6 receiver.
- Battery 2 powers the blade rotation system using a buck converter and relay.

### Locomotion System
- Switch 1 powers the Arduino Uno R3, motor driver L298, and Flysky FS-i6 receiver.
- The FS-i6 transmitter sends commands to the FS-i6 receiver, which relays them to the Arduino R3.
- The Arduino processes the commands and sends signals to the motor driver, activating the **DC motors** that control the bot's movement.
  - Forward throttle: Moves the bot forward.
  - Reverse throttle: Moves the bot backward.
  - Turning the throttle left or right: Changes the bot's direction.

### Blade Rotation System
- Switch 2 powers the buck converter, which reduces the voltage from 12V-20A to 12V-10A.
- A relay acts as a switch between the battery and the crop cutting blade system, controlling the power to the MY 6812 motor.
- The relay is triggered via servo connections controlled by the Flysky FS-i6, enabling precise control over the blade's operation.

## Real-Time Application

### Case 1: Cutting of Plants
The crop cutting bot successfully cuts plants, demonstrating its effectiveness in agricultural settings.
![Plant Cutting](https://github.com/user-attachments/assets/7760e8f3-06b2-4969-8074-ca48624e5161)

### Case 2: Plywood Cutting
The bot was tested on plywood, and it successfully cut through a plywood sheet, showing that it is capable of performing more robust tasks.
![wood cutting](https://github.com/user-attachments/assets/3ddd7ecd-e14a-477a-b724-2831cab758ae)

### Case 3: PVC Sheet Cutting
The bot was also tested on a PVC sheet, successfully cutting through it, demonstrating its versatility and practical utility in different applications.
![PVC cutting](https://github.com/user-attachments/assets/227d24f7-7e11-4dbe-8eb1-68dbe09a9b14)

## Conclusion

The development and implementation of the **Crop Cutting Bot** utilizing a PVC pipe body and Arduino technology have shown promising results in agricultural automation. This project addresses the need for efficient and reliable crop cutting methods, particularly in areas where manual labor is intensive and time-consuming.

Key aspects of the design include:
- The use of an Arduino microcontroller as the central control unit, which manages the bot's movement and blade operation.
- Integration of motor drivers for controlling the gear motors for locomotion and the e-bike motor for cutting crops.
- Successful testing and performance evaluations show the bot's potential to reduce labor and streamline agricultural tasks.

The crop cutting bot demonstrated commendable performance in terms of accuracy, speed, and efficiency. It effectively navigates different terrains and cuts crops with ease, showcasing its potential to significantly assist in agricultural processes.

## How to Build

1. Assemble the Motors: Mount the Jonson gear motors using motor mounts and connect them to the motor driver L298.
2. Connect the Motor Driver: Interface the motor driver with the Arduino Uno R3 for controlling the bot’s movement.
3. Setup Flysky FS-i6: Configure the Flysky FS-i6 transmitter and receiver for sending and receiving movement commands.
4. Crop Cutting Mechanism: Mount the e-bike brush motor and attach it to the crop cutting blade. Use a relay to control the motor's power.
5. Power System: Use two separate lithium-ion batteries:
   - One for the locomotion system (connected to Arduino and motors).
   - One for the blade rotation system (connected via a buck converter and relay).
6. Wiring and Power Management: Ensure proper wiring of all components, including the connection of the relay and buck converter for blade control.
7. Programming: Upload the Arduino code to handle the control signals from the FS-i6 and manage the motor driver and relay system.
8. Testing and Adjustments: Test the bot for movement and crop cutting. Make any necessary adjustments to the blade and motor speed to ensure efficient cutting.

## License

This project is licensed under the MIT License. 
