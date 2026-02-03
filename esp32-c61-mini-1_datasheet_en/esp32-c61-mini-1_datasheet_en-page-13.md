**Title:**
3 Pin Definitions

**Table Title and Source Note (continued from previous page):**
Table 4 – cont’d from previous page

| Name | No. | Type^2 | Function |
|------|-----|--------|----------|
| IO25 | 24  | I/O/T   | GPIO25, SDIO_CMD |
| IO26 | 25  | I/O/T   | GPIO26, SDIO_CLK |
| IO27 | 26  | I/O/T   | GPIO27, SDIO_DATA0 |
| IO28 | 27  | I/O/T   | GPIO28, SDIO_DATA1 |
| IO22 | 28  | I/O/T   | GPIO22, SDIO_DATA2 |
| IO23 | 29  | I/O/T   | GPIO23, SDIO_DATA3 |
| RXO  | 30  | U/OT    | UORXD, GPIO10 |
| TXO  | 31  | U/OT    | UOTXD, GPIO11 |
| ANT24| 44  | I/O     | RF input and output |

**Footnotes:**
- ^2 P: power supply; I: input; O: Output; T: high impedance.
- ^3 In modules with embedded SPI PSRAM, this pin is already used as SPIC51 for SPI PSRAM and cannot be used for other functions. In modules without embedded SPI PSRAM, this pin can be used as GPIO14.

**Additional Information Note (with hyperlink):**
By default, ESP32-C61-MINI-1U uses ANT1, and ANT2 is disabled. To use ANT2, please [contact us](#).

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:**  
ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6