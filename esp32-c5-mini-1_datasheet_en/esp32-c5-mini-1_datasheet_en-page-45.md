**Title:**
9 Peripheral Schematics

**Body Text:**

This is the typical application circuit of the module connected with peripheral components (for example, power supply, antenna, reset button, JTAG interface, and UART interface).

- Please control the voltage levels of strapping pins. For more details, please refer to Chapter 4 Boot Configurations.
  
- Soldering the EPAD to the ground of the base board is not a must; however, it can optimize thermal performance. If you choose to solder it, please apply the correct amount of soldering paste. Too much soldering paste may increase the gap between the module and the baseboard. As a result, the adhesion between other pins and the baseboard may be poor.

- To ensure that the power supply to the ESP32-C5 chip is stable during power-up, it is advised to add an RC delay circuit at the EN pin. The recommended setting for the RC delay circuit is usually R = 10 kΩ and C = 1 μF. However, specific parameters should be adjusted based on the power-up timing of the module and the power-up and reset sequence timing of the chip.

**Figure Caption:**
Figure 9-1. ESP32-C5-MINI-1 Peripheral Schematics

**Footer Text:**
Espressif Systems
45 Submit Documentation Feedback
ESP32-C5-MINI-1 Datasheet v1.0