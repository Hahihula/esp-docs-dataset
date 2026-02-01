**Title: ESP32-S3 Series Comparison**

---

### Section 1

#### Nomenclature (1.1)

- **ESP32-S3**
- F, H/N, x, R, H, V
  
  - 1.8 V external SPI flash only
  - PSRAM size (MB)
  - PSRAM temperature: High temperature
  - Flash:
    - N: Normal temperature

**Figure Caption:** Figure 1-1. ESP32-S3 Series Nomenclature

---

### Section 2

#### Comparison (1.2)

| Part Number | In-Package Flash | In-Package PSRAM | Ambient Temp. | VDD_SPI Voltage | Chip Revision |
|-------------|------------------|------------------|---------------|-----------------|--------------|
| ESP32-S3   | —                | —                | -40 ~ 105 °C | 3.3 V/1.8 V      | v0.1/v0.2    |
| ESP32-S3FN8 |                   |                  |              |                 |             |
| ESP32-S3RH2 |                   |                  | -40 ~ 105 °C | 3.3 V           | v0.2         |
| ESP32-S3R8  |                   |                  | -40 ~ 65 °C   |                 |             |
| ESP32-S3R16V|                   |                  |              | 1.8 V           | v0.2         |
| ESP32-S3FH4R2|                |                  | -40 ~ 85 °C   | 3.3 V           | v0.1/v0.2    |
| ESP32-S3R8V (EOL) |               |                 |              | 1.8 V          | v0.1/v0.2    |
| ESP32-S3R2 (EOL)|                |                  | -40 ~ 65 °C   | 3.3 V           | v0.1/v0.2    |

**Footnotes:**
1 For details on chip marking and packing, see Section [7 Packaging](#).
2 Information about in-package flash; also refer to Section [4.1.2.1 Internal Memory](#). By default, the SPI flash operates at a maximum clock frequency of 80 MHz without auto suspend feature.
3 Ambient temperature specifies recommended range for environment outside ESPRESSIF chip. For chips with OTP SPI PSRAM (ESP32-S3R8, ESP32-S3R8V and ESP32-S3R16V), if the PSRAM ECC function is enabled; maximum ambient can be improved to 85 °C while usable size of PSRAM will reduce by a factor.
4 For more information on VDD_SPI see Section [2.5 Power Supply](#).
5 Details about SPI modes, refer to Section [2.6 Pin Mapping Between Chip and Flash/PSRAM](#).
6 ESP32-S3R2 has been upgraded; for further details please visit PCN.

---

**Footer:**  
Espressif Systems  
13  
[Submit Documentation Feedback](#)