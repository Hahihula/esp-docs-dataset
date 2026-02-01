**Title: ESP32-C5 Series Information**

---

### Section 1

#### Subsection Title: Nomenclature (1.1)

- **Diagram Description:** 
  - The diagram shows the nomenclature for different types of chips in the ESP32-C5 series.
  - Labels include:
    - H/N
    - F/R
    - X
  - Arrows point to descriptions such as "In-package flash or PSRAM size," "In-package flash," and so on.

- **Diagram Caption:**
  Figure 1-1. ESP32-C5 Series Nomenclature

---

### Section 2 (1.2)

#### Subsection Title: Series Information

**Table Description:** 
- The table provides information about the different parts of the ESP32-C5 series, including ambient temperature ranges and in-package flash/PSRAM sizes.

| Part Number | Ambient Temp. (°C) | In-Package Flash 1 | In-Package PSRAM 4 | Package |
|-------------|--------------------|---------------------|--------------------|---------|
| ESP32-C5HR8 | -40 ~ 105          | —                   | 8 MB (Quad SPI)    | QFN48 (6×6 mm) |
| ESP32-C5HF4 |                    | 4 MB (Quad SPI)    | —                  |         |

**Table Notes:**
1. For details on chip marking and packing, see Section [7 Packaging](#).
2. Ambient temperature specifies the recommended temperature range of the environment outside an Espressif chip.
3. For information about in-package flash, also refer to Section 4.1.2.1 Internal Memory (link). By default, the SPI flash on the chip operates at a maximum clock frequency of 80 MHz and does not support auto suspend feature. If you need higher frequencies or an auto suspend function for your application, please contact us.
4. For details about SPI modes, see Section [2.6 Pin Mapping Between Chip and Flash/PSRAM](#).

---

**Footer:**
- Espressif Systems
- Page number 14 (bottom right)
- Document version ESP32-C5 Series Datasheet v1.0

**Link Texts in Table Notes:** 
- Section [7 Packaging](#)
- contact us.
- Section [2.6 Pin Mapping Between Chip and Flash/PSRAM](#)