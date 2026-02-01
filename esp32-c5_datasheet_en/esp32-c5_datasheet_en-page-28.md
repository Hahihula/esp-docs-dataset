**Title:**
2 Pins

**Subtitle:**
2.6 Pin Mapping Between Chip and Flash/PSRAM

**Body Text:**
Table 2-12 lists the pin mapping between the chip and off-package flash/PSRAM for all SPI modes. It can also serve as a reference for chip variants with in-package flash/PSRAM.

For more information on SPI controllers, see also Section 4.2.1.2 SPI Controller.

**Notice:**
It is not recommended to use the pins connected to flash/PSRAM for any other purposes.

**Table Title and Content (Table 2-12): Pin Mapping Between Chip and Off-Package Flash**

| QFN40 | Pin Name       | Single SPI      | Dual SPI     | Quad SPI |
|-------|----------------|------------------|--------------|----------|
| 31    | SPICLK         | flash           | CLK          |          |
| 26    | SPICSO¹        | CS#              | CS#          |          |
| 32    | SPID           | MOSI             | SIOO²        | I00      |
| 27    | SPIQ           | MISO             | SI01         | I01      |
| 28    | SPIWP          | WP#              | SO2          |         |
| 30    | SPIHD          | HOLD#            | S03          |         |

¹ SPICSO is used to access flash
² SIO: Serial Data Input and Output

**Table Title and Content (Table 2-13): Pin Mapping Between Chip and Off-Package PSRAM**

| QFN48 | Pin Name       | Single SPI      | Quad SPI |
|-------|----------------|------------------|----------|
| 31    | SPICLK         | flash           | CLK      |
| 25    | SPICS¹         | CE#              | CS#      |
| 32    | SPID           | SI²             | SIOO     |
| 27    | SPIQ           | SO³              | SI01     |
| 28    | SPIWP          | SIO2             |         |
| 30    | SPIHD          | SIO3             |         |

¹ SPICS1 is used to access PSRAM

² SI: Serial Data Input, equivalent to MOSI
³ SO: Serial Data Output, equivalent to MISO

**Footer Information:**
Espressif Systems  
ESP32-C5 Series Datasheet v1.0  

**Link Text at the bottom of page:**  
Submit Documentation Feedback