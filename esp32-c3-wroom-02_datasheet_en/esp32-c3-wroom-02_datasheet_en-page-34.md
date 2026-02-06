**Title:**
9 Peripheral Schematics

**Body Text:**

This is the typical application circuit of the module connected with peripheral components (for example, power supply, antenna, reset button, JTAG interface, and UART interface).

**Figure Caption:**  
Figure 9-1. Peripheral Schematics

**Diagram Description in Image:**
The diagram shows a schematic layout for connecting various peripherals to an ESP32-C3 module via the WROOM-02 or WROOM-02U package.

**Additional Text Below Diagrams and Components (in Markdown format):**

Soldering the EPAD to the ground of the base board is not a must, however, it can optimize thermal performance. If you choose to solder it, please apply the correct amount of soldering paste. Too much soldering paste may increase the gap between the module and the baseboard. As a result, the adhesion between other pins and the baseboard may be poor.

To ensure that the power supply to the ESP32-C3 chip is stable during power-up, it is advised to add an RC delay circuit at the EN pin. The recommended setting for the RC delay circuit is usually R = 10 kΩ and C = 1 μF. However, specific parameters should be adjusted based on the power-up timing of the module and the power-up and reset sequence timing of the chip. For ESP32-C3's power-up and reset sequence timing diagram, please refer to Section **4.3 Chip Power-up and Reset**.

UART0 is used to download firmware and log output. When using the AT firmware, note that the UART GPIO is already configured. It is recommended to use the default configuration. Please refer to ESP-AT User Guide for ESP32-C3 > Section Hardware Connection.

**Footer:**
Espressif Systems  
Page 34  
ESP32-C3-WROOM-02 & WROOM-02U Datasheet v1.6

**Link:** Submit Documentation Feedback