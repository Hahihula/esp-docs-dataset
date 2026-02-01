Title: Peripheral Schematics

Body Text:
This is the typical application circuit of the module connected with peripheral components (for example, power supply, antenna, reset button, JTAG interface, and UART interface).

Caption under image:

Figure 9-1. Peripheral Schematics

List items below caption include detailed explanations about soldering EPAD to ground for thermal performance optimization; ensuring stable chip during power-up by adding an RC delay circuit at EN pin with recommended settings (R = 10 kΩ, C = 1 μF); and instructions on adjusting parameters based on the module's specific timing. It also mentions using UART0 for downloading firmware and log output.

- Soldering EPAD to ground is optional but can optimize thermal performance.
- To ensure stable power-up of ESP32-C3 chip during initial boot, add an RC delay circuit at EN pin with recommended settings (R = 10 kΩ, C = 1 μF).
- Adjust parameters based on the module's specific timing and refer to Section Chip Power-up and Reset for more details.
- UART0 is used for downloading firmware. When using AT firmware note that UART GPIO configuration may differ from default.

Hyperlinks:
- ESP-AT User Guide for ESP32-C3
- Section Hardware Connection

Footer text includes the page number (35) along with a link to submit documentation feedback and mentions "ESP32-C3-MINI-1 & MINI-1U Datasheet v2.1".