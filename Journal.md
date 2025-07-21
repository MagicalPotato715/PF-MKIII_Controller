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

# July 22th: Begin Schematic / Making Symbols * Footprints



