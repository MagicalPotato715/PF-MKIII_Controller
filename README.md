****PF-MKIII_Controller****
-----

About: This is the handheld controller for the third-generation of my hexapod project: Pathfinder. This controller features left and right hall effect joysticks - for rotation and movement, respectively. There are also three latch buttons for ON/OFF control of autonomous movement, the hexapod, and the controller itself - alongside numerous miscellaneous status LEDs. Additionally, to communicate with the hexapod, the controller uses an NRF Chip as the main transmitter and an Arduino ESP32 Nano as the MCU. 
---

Why: Pathfinder MK-III itself has an NRF transmitter onboard. Since it's supposed to operate with Inverse Kinematics (live movement), the only options for controls are to either set up a wifi connection with a computer or through a controller. Since the hexapod's MCU, the STM32-f446re, doesn't support wireless code uploading, the only option is through a controller.
---

<img width="1090" height="670" alt="Screenshot 2025-07-28 at 10 32 58 AM" src="https://github.com/user-attachments/assets/10a88e61-204d-4bb9-ac2a-2325b2393f07" />
<img width="579" height="558" alt="Screenshot 2025-07-28 at 10 33 16 AM" src="https://github.com/user-attachments/assets/307f4f04-8022-4e64-9033-a2e46473668c" />
<img width="697" height="665" alt="Screenshot 2025-07-28 at 10 33 49 AM" src="https://github.com/user-attachments/assets/a0cad91a-647e-43ee-a460-1564fcc21970" />


Bill Of Materials
-----
|Component|Quantity|Model|Lowest Price|Link|
|---|---|---|---|---|
|Dev Board|1|Arduino ESP32 Nano|$11.79|[Link](https://www.aliexpress.com/item/3256807939051766.html?spm=a2g0o.cart.0.0.725738daz9Ksmg&mp=1&pdp_npi=5%40dis%21USD%21USD%2020.26%21USD%2012.56%21%21USD%2012.56%21%21%21%40210156fc17536786169312567e890e%2112000043892831353%21ct%21US%216187826129%21%211%210)|
|Battery|1|3.7v lipo|$5.16|[Link](https://www.aliexpress.com/item/3256808941846105.html?spm=a2g0o.cart.0.0.725738daz9Ksmg&mp=1&pdp_npi=5%40dis%21USD%21USD%205.16%21USD%205.16%21%21USD%205.16%21%21%21%400b1bf20817536788724595407e3676%2112000048014338867%21ct%21US%216187826129%21%211%210)|
|Joysticks|2 (1x5pcs)|09032|$5.3|[Link](https://www.aliexpress.com/item/3256808542713532.html?spm=a2g0o.cart.0.0.725738daz9Ksmg&mp=1&pdp_npi=5%40dis%21USD%21USD%2010.98%21USD%205.38%21%21USD%205.38%21%21%21%400b1bf20817536788724595407e3676%2112000046421716696%21ct%21US%216187826129%21%211%210)|
|NRF Transmitter|1|NRF24L01+|$2.30|[Link](https://www.aliexpress.com/item/3256805495903750.html?spm=a2g0o.productlist.main.2.6555405a81EXOg&algo_pvid=4da61190-12b2-4f13-9f49-e5557cba752b&algo_exp_id=4da61190-12b2-4f13-9f49-e5557cba752b-1&pdp_ext_f=%7B%22order%22%3A%222066%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%211.37%211.37%21%21%219.77%219.77%21%40212a6e2917536789864826848eb8be%2112000033996194288%21sea%21US%216187826129%21X&curPageLogUid=BgwmNtiZJQbL&utparam-url=scene%3Asearch%7Cquery_from%3A)|
|Latch Button|3 (1x10pcs)|6Pin Push Tactile|$1.29|[Link](https://www.aliexpress.com/item/2255800510764155.html?spm=a2g0o.cart.0.0.79d738daWxrOFF&mp=1&pdp_npi=5%40dis%21USD%21USD%201.29%21USD%201.29%21%21USD%201.29%21%21%21%40212a70c117536791531033590e52c9%2110000006101802626%21ct%21US%216187826129%21%211%210)|
|OLED Screen|1|SSD1306|$2.05|[Link](https://www.aliexpress.com/item/3256805954920554.html?spm=a2g0o.cart.0.0.79d738daWxrOFF&mp=1&pdp_npi=5%40dis%21USD%21USD%202.05%21USD%202.05%21%21USD%202.05%21%21%21%40212a70c117536791531033590e52c9%2112000035944225408%21ct%21US%216187826129%21%211%210)|
|Button|1|PBS-33B-G-X|$3.19|[Link](https://www.aliexpress.com/item/3256807265866776.html?spm=a2g0o.cart.0.0.79d738daWxrOFF&mp=1&pdp_npi=5%40dis%21USD%21USD%203.19%21USD%203.19%21%21USD%203.19%21%21%21%40212a70c117536791531033590e52c9%2112000040814174970%21ct%21US%216187826129%21%211%210)|
|RGB LED|2 (1x50pcs)|Common Cathode|$2.40|[Link](https://www.aliexpress.com/item/3256807678016250.html?spm=a2g0o.cart.0.0.79d738daWxrOFF&mp=1&pdp_npi=5%40dis%21USD%21USD%203.63%21USD%202.40%21%21USD%202.40%21%21%21%40212a70c117536791531033590e52c9%2112000042596159855%21ct%21US%216187826129%21%211%210)|
|Resistor Pack|1|510R, 44.7KR|$5.61|[Link](https://www.aliexpress.com/item/3256807883956541.html?spm=a2g0o.productlist.main.2.143211f2uS3ioA&algo_pvid=a85366f6-d296-4a62-9b70-adf952553cac&algo_exp_id=a85366f6-d296-4a62-9b70-adf952553cac-1&pdp_ext_f=%7B%22order%22%3A%22258%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%218.38%215.61%21%21%2159.73%2140.00%21%40213ba0c517536799111818556ea347%2112000043532036113%21sea%21US%216187826129%21X&curPageLogUid=7XvXStSYsJtD&utparam-url=scene%3Asearch%7Cquery_from%3A#nav-specification)|
|10uF Capacitor|1|0805W106K250CC|$0.6|[Link](https://www.aliexpress.com/item/1626652703.html?spm=a2g0o.productlist.main.1.48fb6316RMeZBk&algo_pvid=e693861e-0391-4f51-8de6-32cd16f941e8&algo_exp_id=e693861e-0391-4f51-8de6-32cd16f941e8-0&pdp_ext_f=%7B%22order%22%3A%22290%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%210.60%210.60%21%21%210.60%210.60%21%402102f22c17525900041745529e7ed1%2165044401121%21sea%21TW%216187826129%21ABX&curPageLogUid=cULtsx9Twjzu&utparam-url=scene%3Asearch%7Cquery_from%3A)|
|0.1uF Capacitor|2 (1x100pcs)|0603B104K250SD|$0.95|[Link](https://www.aliexpress.com/item/1005003512666695.html?spm=a2g0o.productlist.main.2.bb674964zgo3zW&aem_p4p_detail=202507151825544677393916540000689187&algo_pvid=30290dc5-6cab-4384-9250-c0f4dd7da1ce&algo_exp_id=30290dc5-6cab-4384-9250-c0f4dd7da1ce-1&pdp_ext_f=%7B%22order%22%3A%2266%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%210.95%210.95%21%21%210.95%210.95%21%400b1bf20a17526291538932348e9ac6%2112000026122537038%21sea%21TW%216187826129%21ABX&curPageLogUid=3zYrgz8WWygI&utparam-url=scene%3Asearch%7Cquery_from%3A&search_p4p_id=202507151825544677393916540000689187_1)|
|LED|2 (1x50pcs)|Green|$1.49|[Link](https://www.aliexpress.com/item/3256806082739727.html?spm=a2g0o.productlist.main.20.58265d61KYx3M3&algo_pvid=2888cd1a-db46-49cb-bcd1-dad9a1187035&algo_exp_id=2888cd1a-db46-49cb-bcd1-dad9a1187035-17&pdp_ext_f=%7B%22order%22%3A%22253%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%212.66%211.76%21%21%2118.96%2112.51%21%402102f22c17536801089633238e9268%2112000036543284014%21sea%21US%216187826129%21X&curPageLogUid=MgZMrUkmbKE4&utparam-url=scene%3Asearch%7Cquery_from%3A)|
|PCB|1||$41.41|JLCPCB Order|

Total Components Price: $61.50
PCB Price: $41.41
Total Price: $102.91
