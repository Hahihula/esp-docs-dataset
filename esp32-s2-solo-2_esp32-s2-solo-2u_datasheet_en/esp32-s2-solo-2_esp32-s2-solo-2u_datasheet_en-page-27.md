**Title:**
8 Peripheral Schematics

**Body Text:**

This is the typical application circuit of the module connected with peripheral components (for example, power supply, antenna, reset button, JTAG interface, and UART interface).

**Figure Caption:**
Figure 8-1. Peripheral Schematics

**List Items:**
- Soldering the EPAD to the ground of the base board is not a must; however, it can optimize thermal performance. If you choose to solder it, please apply the correct amount of soldering paste. Too much soldering paste may increase the gap between the module and the baseboard. As a result, the adhesion between other pins and the baseboard may be poor.
- To ensure that the power supply to the ESP32-S2 chip is stable during power-up; it is advised to add an RC delay circuit at the EN pin. The recommended setting for the RC delay circuit is usually R = 10 kΩ and C = 1 μF. However, specific parameters should be adjusted based on the power-up timing of the module and the power-up and reset sequence timing of the chip.

**Reference:**
For ESP32-S2’s power-up and reset sequence timing diagram, please refer to **ESP32-S2 Series Datasheet > Section Power Scheme.**

**Footer Information:**
Espressif Systems
Page 27

**Link Text at Bottom Right Corner:**
Submit Documentation Feedback