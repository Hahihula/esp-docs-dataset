Title: ESP32-C3 Series Comparison

Subtitle:
1.1 Nomenclature

Diagram Description (Figure Caption):
- Figure 1-1 illustrates "ESP32-C3 Series Nomenclature".
- The diagram shows a block labeled "ESP32-C3" with arrows pointing to different labels such as F, H/N, x, AZ.
- Additional information includes:
  - Other Identification Code
  - Flash size (MB)
  - Flash temperature: High temperature or Normal temperature

Subtitle:
1.2 Comparison

Table Title and Description:
- Table 1-1 lists the "ESP32-C3 Series Comparison".
- The table has columns for Ordering Code, In-Package Flash, Ambient Temp., Package (mm), GPIO No., Chip Revision.

Table Content:

| Ordering Code | In-Package Flash | Ambient Temp. (°C) | Package (mm)    | GPIO No. 6 | Chip Revision |
|---------------|------------------|--------------------|-----------------|------------|--------------|
| ESP32-C3     | —                | -40 ~ 105          | QFN32 (5*5)     | 22         | v0.4         |
| ESP32-C3FN4   | End of life      | 4 MB               | QFN32 (5*5)     | 22         | v0.4         |
| ESP32-C3FH4   | —                | -40 ~ 105          | QFN32 (5*5)     | 22         | v0.4         |
| ESP32-C3FH4AZ | NRND             | 4 MB               | QFN32 (5*5)     | 16         | v0.4         |
| ESP32-C3FH4X  | —                | -40 ~ 105          | QFN32 (5*5)     | 16         | v1.1         |

Footnotes:
1 For details on chip marking and packing, see Section [7 Packaging](#).
2 Ambient temperature specifies the recommended temperature range of the environment immediately outside an Espressif chip.
3 For information about in-package flash, also refer to Section [4.1.2.1 Internal Memory](#). By default, the SPI flash operates at a maximum clock frequency of 80 MHz and does not support auto suspend feature. If you have requirements for higher flash clock frequency or need automatic flash suspend features please contact us.
4 All chip revisions share same SRAM size but with different revision v1.1 (e.g., ESP32-C3FH4X) has around ~10 KB more available space than previous version, and it depends on specific ESP-IDF versions as detailed in [Compatibility Advisory for ESP32-C3 Chip Revision v1.1](#). For how to identify chip revisions please refer to [ESP32-C3 Series SoC Errata](#).
5 ESP32-C3 requires an SPI flash off the chip's package, and details about different modes can be found in Section 2.6 Pin Mapping Between Chip and Flash.
6 SPI0/SPI1 pins for flash connection are not bonded to variants with 16 GPIOs.

Footer:
- Page number: "12"
- Document title or section reference at the bottom right corner, which is partially cut off but appears as "[ESP32-C3 Series Datasheet v2.2](#)".
- Link for submitting documentation feedback labeled "Submit Documentation Feedback".