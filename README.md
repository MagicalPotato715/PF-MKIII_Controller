****PF-MKIII_Controller****
-----

About: This is the handheld controller for the third-generation of my hexapod project: Pathfinder. This controller features left and right hall effect joysticks - for rotation and movement, respectively. There are also three latch buttons for ON/OFF control of autonomous movement, the hexapod, and the controller itself - alongside numerous miscellaneous status LEDs. Additionally, to communicate with the hexapod, the controller uses an NRF Chip as the main transmitter and an Arduino ESP32 Nano as the MCU. 
---

Why: Pathfinder MK-III itself has an NRF transmitter onboard. Since it's supposed to operate with Inverse Kinematics (live movement), the only options for controls are to either set up a wifi connection with a computer or through a controller. Since the hexapod's MCU, the STM32-f446re, doesn't support wireless code uploading, the only option is through a controller.
---

<img width="1090" height="670" alt="Screenshot 2025-07-28 at 10 32 58 AM" src="https://github.com/user-attachments/assets/10a88e61-204d-4bb9-ac2a-2325b2393f07" />
<img width="579" height="558" alt="Screenshot 2025-07-28 at 10 33 16 AM" src="https://github.com/user-attachments/assets/307f4f04-8022-4e64-9033-a2e46473668c" />
<img width="697" height="665" alt="Screenshot 2025-07-28 at 10 33 49 AM" src="https://github.com/user-attachments/assets/a0cad91a-647e-43ee-a460-1564fcc21970" />
