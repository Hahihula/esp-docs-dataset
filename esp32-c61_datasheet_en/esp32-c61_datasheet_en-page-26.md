**Title:**
2 Pins

**Table Title:**
Table 2-12. Pin Mapping Between Chip and Off-Package PSRAM^1

| Pin No. | Pin Name       | Single SPI PSRAM | Quad SPI PSRAM |
|---------|----------------|------------------|-----------------|
|         |                |                  |                 |
| 26      | SPICLK         | CLK              | CLK             |
| 19      | SPICS1^2       | CE#               | CE#             |
| 27      | SPIID          | SI3               | SIO0            |
| 22      | SPIQ           | SO4               | SIO1            |
| 23      | SPIWP          |                  |                 |
| 25      | SPIHD          |                  |                 |

**Footnotes:**
^1 An off-package PSRAM can only be connected if the chip variant does not have an on-package PSRAM. If PSRAM is not connected, these pins cannot be used as GPIO pins.
^2 SPICS1 is used to access PSRAM
^3 SI: Serial Data Input, equivalent to MOSI
^4 SO: Serial Data Output, equivalent to MISO

**Footer:**
Espressif Systems 26 ESP32-C61 Series Datasheet v0.5