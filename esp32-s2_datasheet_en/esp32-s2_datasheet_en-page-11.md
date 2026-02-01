**Title: ESP32-S2 Series Comparison**

---

### Section 1

#### Subsection Title: Nomenclature (1.1)

- **Diagram Description:** 
  - The diagram shows the nomenclature for different parts of an ESP32-S2 chip.
  - Labels include "ESP32-S2", followed by letters and symbols such as F, H/N, X, R with corresponding PSRAM size in MB (e.g., PSRAM), Flash size in MB (e.g., Flash), temperature conditions indicated for high or normal temperatures.

- **Figure Caption:**
  - Figure caption is "Figure 1-1. ESP32-S2 Series Nomenclature"

---

### Section 2

#### Subsection Title: Comparison (1.2)

**Table Description:** 
- The table compares different parts of the ESP32-S2 series based on in-package flash, PSRAM size and type, ambient temperature range, and VDD_SPI voltage.

| Part Number | In-Package Flash^5 | In-Package PSRAM | Ambient Temp.^2  | VDD_SPI Voltage^3 |
|-------------|---------------------|------------------|------------------|--------------------|
| ESP32-S2    | —                   | —                | -40 ~ 105 °C     | 3.3 V/1.8 V        |
| ESP32-S2FH2 | 2 MB (Quad SPI)^4   | —                | -40 ~ 105 °C     | 3.3 V             |
| ESP32-S2FH4 | 4 MB (Quad SPI)    | —                | -40 ~ 105 °C     | 3.3 V             |
| ESP32-S2FN4R2| 4 MB (Quad SPI)    | 2 MB (Quad SPI) | -40 ~ 85 °C      | 3.3 V             |
| ESP32-S2R2  | —                   | 2 MB (Quad SPI) | -40 ~ 85 °C      | 3.3 V             |

**Footnotes:**
1. For details on chip marking and packing, see Section 7 [Packaging](#).
2. Ambient temperature specifies the recommended temperature range of the environment immediately outside an Espressif chip.
3. For more information on VDD_SPI, see Section **2.5 Power Supply**.
4. For details about SPI modes, see Section **2.6 Pin Mapping Between Chip and Flash/PSRAM**.

---

**Footer:**
- "Espressif Systems"
- Page number 11
- Document title is ESP32-S2 Series Datasheet v1.8

**Link:** Submit Documentation Feedback