**Title: Module Overview**

---

### Table 1-2. ESP32-C3-MINI-1U (CONN) Series Comparison

| Ordering Code | Flash Size | Ambient Temp. (°C) | Chip Revision | Size (mm) |
|----------------|------------|--------------------|---------------|-----------|
| **ESP32-C3-MINI-1U-N4X** <br> *(Recommended)* | 4 MB (Quad SPI) | -40 ~ 85 | v1.1 | 13.2 x 12.5 x 2.4 |
| **ESP32-C3-MINI-1U-H4X** <br> *(Recommended)* | 4 MB (Quad SPI) | -40 ~ 105 | v1.1 | 13.2 x 12.5 x 2.4 |
| **ESP32-C3-MINI-1U-N4** *(NRND)* | <br> | -40 ~ 85 | v0.4 | 16.9 x 17.0 x 2.4 |
| **ESP32-C3-MINI-1U-H4** *(NRND)* | <br> | -40 ~ 105 | v0.4 | 16.9 x 17.0 x 2.4 |

*Ambient temperature specifies the recommended temperature range of the environment immediately outside the Espressif module.*

For details, refer to Section [10.1 Module Dimensions](#).

The flash is integrated in the chip's package. For specifications, refer to Section [6.5 Memory Specifications](#).

All modules can be pre-programmed with AWS IoT ExpressLink firmware. Modules with such firmware have suffix "-A" in their ordering codes (e.g., ESP32-C3-MINI-1U-N4-A). Since AWS IoT ExpressLink firmware enables flash encryption and secure boot, joint download boot mode will be disabled, and it will no longer be possible to program firmware through the UART or USB port into the modules.

All chip revisions have the same SRAM size, but chip revision v1.1 has around 10 KB more available space for users than chip revision v0.4. Chip revision v1.1 depends on specific ESP-IDF versions, as detailed in [Compatibility Advisory for ESP32-C3 Chip Revision v1.1](#). For how to identify chip revisions, please refer to [ESP32-C3 Series SoC Errata](#).

By default, the SPI flash on the module operates at a maximum clock frequency of 80 MHz and does not support auto suspend feature. If you have a requirement for higher flash clock frequency or if need the flash auto suspend feature, please contact us.

Both ESP32-C3-MINI-1U and ESP32-C3-MINI-1U has two operating ambient temperature options: -40 ~ 85 °C variants and -40 ~ 105 °C variants, all embedded with the ESP32-C3FH4 chip. ESP32-C3-MINI-1 has one more variant: ESP32-C3-MINI-1H4-AZ embedded with the ESP32-C3FH4AZ chip. For this chip, SPI0/SP1 pins for flash connection are not bonded. For more information about the differences between chips embedded, please refer to Section [Chip Series Comparison in ESP32-C3 Series Datasheet](#).

---

### 1.3 Applications

- Smart Home
- Industrial Automation
- Health Care
- Consumer Electronics
- Smart Agriculture
- POS Machines
- Service Robot
- Audio Devices
- Generic Low-power IoT Sensor Hubs
- Generic Low-power IoT Data Loggers