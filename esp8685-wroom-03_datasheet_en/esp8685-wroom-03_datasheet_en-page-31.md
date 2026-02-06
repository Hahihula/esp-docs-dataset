**Title:**
9 Peripheral Schematics

**Body Text:**

This is the typical application circuit of the module connected with peripheral components (for example, power supply, antenna, reset button, JTAG interface, and UART interface).

EN on the module is pulled up to VDD33 through a 10 kΩ resistor, and connected to GND through a 1 uF capacitor.

**Figure Caption:**
Figure 9-1. Peripheral Schematics

**Additional Information in Image (Schematic Diagram):**

- ESP8685-WROOM-03
- Components labeled with their respective pins:
  - EN
  - IO4, IO5, TXD, RXD, GND, 3V3
  - C1: 10uF capacitor connected to ground (GND)
  - C2 and R2 forming a resistor network for power-up stabilization

**Subsection Texts with Bullet Points:**

- To ensure that the power supply to the ESP8685 chip is stable during power-up, it is advised to add an RC delay circuit at the EN pin. The recommended setting for the RC delay circuit is usually R = 10 kΩ and C = 1 μF (such RC delay circuit has already been built into the module). However, specific parameters should be adjusted based on the power-up timing of the module and the power-up and reset sequence timing of the chip. For ESP8685’s power-up and reset sequence timing diagram, please refer to Section **4.3 Chip Power-up and Reset**.

- UART0 is used to download firmware and log output. When using the AT firmware, note that the UART GPIO is already configured. It is recommended to use the default configuration. Please refer to ESP-AT User Guide for ESP32-C3 > Section Hardware Connection.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP8685-WROOM-03 Datasheet v1.5