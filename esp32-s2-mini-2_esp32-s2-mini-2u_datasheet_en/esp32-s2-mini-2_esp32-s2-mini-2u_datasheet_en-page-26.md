**Title:**
8 Peripheral Schematics

**Body Text:**

This is the typical application circuit of the module connected with peripheral components (for example, power supply, antenna, reset button, JTAG interface, and UART interface).

- **Soldering**: The EPAD to the ground of the base board is not a must; however, it can optimize thermal performance. If you choose to solder it, please apply the correct amount of soldering paste. Too much soldering paste may increase the gap between the module and the baseboard.
  
- To ensure that the power supply to the ESP32-S2 chip is stable during power-up, it’s advised to add an RC delay circuit at the EN pin.

**Additional Information:**
- The recommended setting for the RC delay circuit in this case usually involves R = 10 kΩ and C = 1 μF. However, specific parameters should be adjusted based on the chip's timing of power-up.
  
For ESP32-S2’s power-up and reset sequence:
- **Timing Diagram**: Please refer to [ESP32-S2 Series Datasheet > Section Power Scheme](#).

**Figure Caption:**
Figure 8-1. Peripheral Schematics

**Footer Text:**
Espressif Systems
Submit Documentation Feedback