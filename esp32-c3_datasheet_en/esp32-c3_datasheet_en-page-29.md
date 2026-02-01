**Title:**
2 Pins

**Subtitle:**
2.6 Pin Mapping Between Chip and Flash

**Body Text:**
Table 2-12 lists the pin mapping between the chip and flash for all SPI modes.

For chip variants with in-package flash (see Table 1-1 ESP32-C3 Series Comparison), the pins allocated for communication with in-package flash can be identified depending on the SPI mode used.

For off-package flash, these are the recommended pin mappings. For more information on SPI controllers, see also Section 4.2.1.2 SPI Controller.

**Notice:**
Do not use the pins connected to in-package flash for any other purposes.

**Table Title:**
Table 2-12. Pin Mapping Between Chip and In-package Flash

| Pin No. | Single SPI Name | Dual SPI Flash | Quad SPI / QPI Flash |
|---------|------------------|-----------------|----------------------|
|         |                  |                 |                      |
| 22      | SPICLK           | CLK             | CLK                  |
| 21      | SPICS0^1        | CS#              | CS#                  |
| 23      | SPID             | DI               | DI                   |
| 24      | SPIQ             | DO               | DO                   |
| 20      | SPIWP            | WP#              | WP#                  |
| 19      | SPIHD            | HOLD#            | HOLD#                |

**Footnote:**
^1 CS0 is for in-package flash

**Footer Information:**
Espressif Systems
Submit Documentation Feedback ESP32-C3 Series Datasheet v2.2