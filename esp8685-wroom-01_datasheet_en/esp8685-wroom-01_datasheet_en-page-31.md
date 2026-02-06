**Title:**
9 Peripheral Schematics

**Body Text:**

This is the typical application circuit of the module connected with peripheral components (for example, power supply, antenna, reset button, JTAG interface, and UART interface).

**Figure Caption:**
Figure 9-1. Peripheral Schematics

**List Items:**
- **Soldering EPAD to the ground:** The board is not a must; however, it can optimize thermal performance. If you choose to solder it, please apply the correct amount of soldering paste. Too much soldering paste may increase the gap between the module and the baseboard. As a result, adhesion between other pins and the baseboard may be poor.
- **Power supply stability:** To ensure that power is supplied during chip power-up for ESP8685 to stable at EN pin delay circuit RC should add an R = 10 kΩ and C = 1 μF (such RC already built into module). However, specific parameters timing of the chip. For ESP8685’s power-up reset sequence diagram please refer Section 4.3 Chip Power-up Reset.
- **UARTO usage:** is used to download firmware log output when using AT firmware note that UART GPIO configuration recommended default configuration Please refer to ESP-AT User Guide for ESP32-C3 > Section Hardware Connection.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP8685-WROOM-01 Datasheet v1.5