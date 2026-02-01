**Title:**
2.6 Pin Mapping Between Chip and Flash/PSRAM

**Body Text:**
Table 2-14 lists the pin mapping between the chip and flash/PSRAM for all SPI modes.

For chip variants with in-package flash/PSRAM (see Table 1-1 ESP32-S2 Series Comparison), the pins allocated for communication with in-package flash/PSRAM can be identified depending on the SPI mode used. For off-package flash/PSRAM, these are the recommended pin mappings.
For more information on SPI controllers, see also Section 4.2.1.2 SPI Controller.

**Notice:**
Do not use the pins connected to in-package flash/PSRAM for any other purposes.

**Table Title:**
Table 2-14. Pin Mapping Between Chip and Flash or PSRAM

| Pin No. | Pin Name       | Single SPI   | Dual SPI    | Quad SPI/QPI | Octal SPI/OPI |
|---------|---------------|--------------|-------------|--------------|---------------|
|         |               | Flash        | Flash       | Flash        | Flash         |
| 29      | SPICS1        | CE#          | CE#         | CE#          | CE#           |
| 31      | SPIHD         | HOLD# SIO3   | HOLD#       | HOLD# SIO3   | DQ3           |
| 32      | SPIWP         | WP# SIO2     | WP#         | WP# SIO2     | DQ2           |
| 33      | SPICSO        | CS#          | CS#         | CS#          |               |
| 35      | SPIQ          | DO           | SO/SIO1     | DO           | DQ1           |
| 36      | SPID          | DI           | SI/SIO0     | DI           | SIO0          |
| 37      | GPIO33        |               |             |              | DQ4           |
| 38      | GPIO34        |               |             |              | DQ5           |
| 39      | GPIO35        |               |             |              | DQ6           |
| 40      | GPIO36        |               |             |              | DQ7           |
| 41      | GPIO37        |               |             |              | DQS/DM        |

**Footnotes:**
1. CSO is for in-package flash
2. CS1 is for in-package PSRAM

**Footer:**
Espressif Systems  
ESP32-S2 Series Datasheet v1.8  
Submit Documentation Feedback