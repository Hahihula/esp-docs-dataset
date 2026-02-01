**Title: Module Overview**

---

### Table 1-1. ESP32-S2-SOLO-2 (ANT) Series Comparison

| Ordering Code | Flash    | PSRAM^3 | Ambient Temp. (°C) | Size^2 (mm) |
|---------------|----------|---------|--------------------|-------------|
| ESP32-S2-SOLO-2-N4   |          |         | -40 ~ 85           |             |
| ESP32-S2-SOLO-2-H4 (End of life) | 4 MB (Quad SPI) | —       | -40 ~ 105          |             |
| ESP32-S2-SOLO-2-N4R2   |          |         |                    | 18.0 x 25.5 x 3.1 |
| ESP32-S2-SOLO-2-N8 (End of life) | 8 MB (Quad SPI) | —       | -40 ~ 85           |             |
| ESP32-S2-SOLO-2-N16   |          |         |                    | 16 MB (Quad SPI)|

**Footnotes:**
1. Ambient temperature specifies the recommended temperature range of the environment immediately outside the Espressif module.
2. For details, refer to Section 9.1 Module Dimensions.
3. For specifications, refer to Section 5.5 Memory Specifications.

---

### Table 1-2. ESP32-S2-SOLO-2U (CONN) Series Comparison

| Ordering Code | Flash    | PSRAM^3 | Ambient Temp. (°C) | Size^2 (mm) |
|---------------|----------|---------|--------------------|-------------|
| ESP32-S2-SOLO-2U-N4  |          |         | -40 ~ 85           |             |
| ESP32-S2-SOLO-2U-H4   |          |         | -40 ~ 105          |             |
| ESP32-S2-SOLO-2U-N4R2 |        2 MB (Quad SPI) | —       |                    | 18.0 x 19.2 x 3.2 |
| ESP32-S2-SOLO-2U-N16   |          |         | -40 ~ 85           |             |

**Footnote:**
4 This table shares the same notes presented in Table 1-1 above.

---

In this datasheet unless otherwise stated, ESP32-S2-SOLO-2 refers to all variants of ESP32-S2-SOLO-2, whereas ESP32-S2-SOLO-2U refers to all variants of ESP32-S2-SOLO-2U. 

At the core of the modules is ESP32-S2 series chip revision v1.0. ESP32-S2 series chips have an Xtensa® 32-bit LX7 CPU that operates at up to 240 MHz. It has a low-power co-processor that can be used instead of the CPU to save power while performing tasks that do not require much computing power, such as monitoring of peripherals.

**Note:**
For more information on ESP32-S2R2, please refer to [ESP32-S2 Series Datasheet](#). For chip revision identification, ESP-IDF release that supports a specific chip revision, and other information on chip revisions, please refer to [ESP32-S2 Series SoC Errata > Section Chip Revision](#).

---

### 1.3 Applications

- Smart Home
- Industrial Automation
- Health Care
- Consumer Electronics (Espressif Systems)
- Smart Agriculture
- POS Machines
- Service Robot
- Audio Devices