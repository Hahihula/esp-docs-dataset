**Title:**
9 Peripheral Schematics

**Body Text:**
This is the typical application circuit of the module connected with peripheral components (for example, power supply, antenna, reset button, JTAG interface, and UART interface).

- **Figure 9-1. Peripheral Schematics**

Soldering the EPAD to the ground of the base board is not a must; however, it can optimize thermal performance. If you choose to solder it, please apply the correct amount of soldering paste. Too much soldering paste may increase the gap between the module and the baseboard.

To ensure that the power supply to the ESP32-C6 chip is stable during power-up, it is advised to add an RC delay circuit at the EN pin. The recommended setting for the RC delay circuit is usually R = 10 kΩ and C = 1 μF; however, specific parameters should be adjusted based on the power-up timing of the module.

**Additional Information:**
For ESP32-C6’s power-up and reset sequence timing diagram, please refer to Section 4.5 Chip Power-up and Reset.

**Footer:**
Espressif Systems
ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4

**Link:**
Submit Documentation Feedback