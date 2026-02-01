**Title:**
2 Pins

**Subtitle:**
2.6 Pin Mapping Between Chip and Flash/PSRAM

**Body Text:**
Table 2-14 lists the pin mapping between the chip and flash/PSRAM for all SPI modes.

For chip variants with in-package flash/PSRAM (see Table 1-1 ESP32-S3 Series Comparison), the pins allocated for communication with in-package flash/PSRAM can be identified depending on the SPI mode used.
For off-package flash/PSRAM, these are the recommended pin mappings. For more information on SPI controllers, see also Section 4.2.1.5 Serial Peripheral Interface (SPI).

**Notice:**
Do not use the pins connected to in-package flash/PSRAM for any other purposes.

**Table Title:**
Table 2-14. Pin Mapping Between Chip and Flash or PSRAM

| Single SPI | Dual SPI | Quad SPI/QPI | Octal SPI/OPI |
|-------------|----------|--------------|---------------|
| **Pin No** | **Pin Name** | **Flash/PSRAM** | **CE#** | **HOLD#** | **SIO3** | **DQ3** | **DQ2** | **CS#** | **WP#** | **SIO2** | **DQ1** |
| 28          | SPICS1   | Flash        | CE#         |            |           |       |      |       |        |         |         |        |
| 30          | SPIHD    | HOLD#       | SIO3       | HOLD#      |           | DQ3     |       |       |        |         |         |        |
| 31          | SPIWP    | WP#         | SIO2       | WP#        |           | DQ2     |       |       |        |         |         |        |
| 32          | SPICSO   | CS#         | CS#        |            |           | CS#     |       |       |        |         |         |        |
| 33          | SPICLK   | CLK         | CLK        |            |           | DQ1     |       |       |        |         |         |        |
| 34          | SPIQ     | DO          | SO/SIO1    | DO         |           | DQ0     |       |       |        |         |         |        |
| 35          | SPID     | DI          | SI/SIOO    | DI         |           | DQ4     |       |       |        |         |         |        |
| 38          | GPIO33   |            |            |            |           | DQ5     |       |       |        |         |         |        |
| 39          | GPIO34   |            |            |            |           | DQ6     |       |       |        |         |         |        |
| 40          | GPIO35   |            |            |            |           | DQ7     |       |       |        |         |         |        |
| 41          | GPIO36   |            |            |            |           | DQ8     |       |       |        |         |         |        |
| 42          | GPIO37   |            |            |            |           | DQS/DM  |       |       |        |         |         |        |

**Footnotes:**
1 CSO is for in-package flash
2 CS1 is for in-package PSRAM

**Footer:**
Espressif Systems  
ESP32-S3 Series Datasheet v2.1  
Submit Documentation Feedback