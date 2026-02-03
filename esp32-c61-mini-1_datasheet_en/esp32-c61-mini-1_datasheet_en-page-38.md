**Title:**
9 Peripheral Schematics

**Figure Title and Description:**
- **Figure**: ESP32-C61-MINI-1U Peripheral Schematics (labeled as Figure 10)

**Body Text with List Items:**

- If an external antenna ANT2 is used, it is recommended to reserve an RF circuit as shown in the figure above. By default, ESP32-C61-MINI-1U uses ANT1, and ANT2 is disabled. To use ANT2, please contact us.

- Soldering the EPAD to the ground of the base board is not a must; however, it can optimize thermal performance. If you choose to solder it, apply the correct amount of soldering paste. Too much soldering paste may increase the gap between the module and the baseboard. As a result, the adhesion between other pins and the baseboard may be poor.

- To ensure that the power supply to the ESP32-C61 chip is stable during power-up, it is advised to add an RC delay circuit at the EN pin. The recommended setting for the RC delay circuit usually R = 10 kΩ and C = 1 μF. However, specific parameters should be adjusted based on the power-up timing of the module and the power-up and reset sequence timing of the chip. For ESP32-C61’s power-up and reset sequence timing diagram, please refer to ESP32-C61 Series Datasheet > Section Power Supply.

- UART0 is used to download firmware and log output. When using the AT firmware, please note that the UART GPIO is already configured. It is recommended to use the default configuration.

**Footer:**
Espressif Systems
Page 38 of ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6

**Link Texts in Body Text (Hyperlinks):**
- contact us.
- ESP32-C61 Series Datasheet > Section Power Supply.

**Note:**
The image contains a schematic diagram with various electronic components and connections, but the text does not provide detailed descriptions of each component or connection.