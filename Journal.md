---
title: "Pathfinder MK-III Handheld Controller"
author: "Calvin Hung"
description: "This is the handheld controller for my hexapod robotics project Pathfinder MKIII. Learn more about Pathfinder MK-III here: https://github.com/MagicalPotato715/Pathfinder-MKIII."
created_at: "7/20/2025"
---

# July 21th: Planning & Research

After searching and deliberation (thinking takes a lot of time), here's the list I came up with for the complete setup.

Hardware:
- Raspberry Pi Pico RP2040 for control
- Left Joystick Rotation
- Right Joystick Movement
- OLED screen for misc displays
- Latch button for Hexapod ON/OFF
- Latch button for eventual Autonomous/Manual
- Momentary Button + LED for Gait Switching
- Lipo + P-Fet system for power from lipo while using USB-C coding
- Comical ON/OFF switch for controller on off
- RGB Status LED for Hexapod Status (On/off/lowpower?)
- NRF24L01+ Reciever to talk to hexapod
- LED to show connection of NRF chip

Software:
- Code Main: take info from buttons etc and transfer to nrf chip.
- LEDs to show hexapod functionality/issues.
- Gait switching shown on OLED
- Gait switching -> each press rotates

This is the (not so) block diagram:
<img width="954" height="533" alt="Screenshot 2025-07-21 at 3 24 50 PM" src="https://github.com/user-attachments/assets/e63b1c92-7cf6-445c-a06d-8801399a497c" />

**Total time spent: 3h**

# July 22th: Begin Schematic & Making Symbols

Learning from my mistakes with the hexapod PCB, I decided to scout out the components (and a seller) before placing them down in Kicad. However, having the block diagram makes it a lot easier to know what to put.

Finished placing down the components! Time to make connections!
<img width="772" height="513" alt="Screenshot 2025-07-21 at 7 52 32 PM" src="https://github.com/user-attachments/assets/1d32644b-1df9-4a3a-ac49-941c3322e173" />

I decided to replace the KY-023 joysticks with these other ps5 joysticks. These new ones don't have a specific part number, but they atleast have a concrete footprint.
![COM-09032_sml](https://github.com/user-attachments/assets/845c6913-5e0f-4672-9e26-20f70065a776)
<img width="544" height="564" alt="Screenshot 2025-07-22 at 3 04 10 PM" src="https://github.com/user-attachments/assets/4636ebe7-a12c-4ca3-af71-855b6d695515" />

I followed this schematic for the joystick wiring.
<img width="582" height="422" alt="Screenshot 2025-07-22 at 3 44 41 PM" src="https://github.com/user-attachments/assets/ab594c75-0d94-421f-ad4e-5004e9ab22fe" />


I also decided to replace the Raspberry Pi Pico with an Arduino ESP32 Nano, because the Pico didn't have enough analog pins. As it turns out, the Arduino ESP32 Nano has exactly what I need!



