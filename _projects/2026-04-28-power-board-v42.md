---
title: Power Board V4.2
description: UBC Thunderbots Electrical Sub-Team
tools: Altium
header:
  overlay_image: /assets/images/Screenshot 2026-04-28 200240.png
---
The robots required a power board rebuild to meet strict size constraints while managing high-voltage noise and maximizing signal integrity in power distribution from our 24V battery pack. As a solution, I coordinated the complete rebuild of the electrical PCB stack-up and revamped the main power board’s spacial constraints. The new design improved the solenoid auto discharge, HV/LV GND plane isolation, voltage regulators, ESP32 MCU, and UI/RasPi connections to ensure manufacturing viability. I personally designed the new HV feedback circuit to monitor discharge noise in order to gauge capacitor storage levels to optimize gameplay efficiency.