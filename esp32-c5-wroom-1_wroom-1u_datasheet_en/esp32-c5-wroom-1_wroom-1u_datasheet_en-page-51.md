Title: Peripheral Schematics

**Figure Caption:**  
Figure 9-2. ESP32-C5-WROOM-1U Schematics

**Body Text with List Items and Emphasis (Note the use of bullet points):**

- If an external antenna ANT2 is used, it is recommended to reserve an RF circuit as shown in the figure above. By default, ESP32-C5-WROOM-1U uses ANT1, and ANT2 is disabled. To use ANT2, please contact us.

- Please control the voltage levels of strapping pins. For more details, please refer to Chapter 4 Boot Configurations.

- Soldering the EPAD to the ground of the base board is not a must; however, it can optimize thermal performance. If you choose to solder it, please apply the correct amount of soldering paste. Too much soldering paste may increase the gap between the module and the baseboard. As a result, the adhesion between other pins and the baseboard may be poor.

- To ensure that the power supply to the ESP32-C5 chip is stable during power-up, it is advised to add an RC delay circuit at the EN pin. The recommended setting for the RC delay circuit is usually R = 10 kΩ and C = 1 μF. However, specific parameters should be adjusted based on the power-up timing of the module and the power-up and reset sequence timing of the chip. For ESP32-C5’s power-up and reset sequence timing diagram, please refer to Section 4.5 Chip Power-up and Reset.

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Page Number:** 
51

**Document Title (at bottom):**
ESP32-C5-WROOM-1 & WROOM-1U Datasheet v0.8 PRELIMINARY