**Title:**
2 Pins

**Subtitle:**
2.6 Pin Mapping Between Chip and Flash

**Body Text:**
Table 2-16 lists the pin mapping between the chip and off-package flash for all SPI modes.

For chip variants with in-package flash (namely variants in QFN32 package, see Table 1-1 ESP32-C6 Series Comparison), the pins allocated for communication with in-package flash are not routed out, but you can take Table 2-16 as a reference.
For more information on SPI controllers, see also Section 4.2.1.2 SPI Controller.

**Notice:**
Do not use the pins connected to flash for any other purposes.

**Table Title:**
Table 2-16. Pin Mapping Between QFN40 Chip and Flash

| GQN40 | Pin Name       | Single SPI   | Dual SPI    | Quad SPI / GPI |
|-------|---------------|--------------|-------------|----------------|
| **Pin No.** | **Flash**     | **Flash**    | **Flash**  | **Flash**      |
| 25    | SPICLK        | CLK          | CLK         | CLK            |
| 20    | SPICS0        | CS#          | CS#         | CS#            |
| 26    | SPID          | MOSI         | SIOO        | SIO0           |
| 21    | SPIQ          | MISO         | SI01        | SI01           |
| 22    | SPIWP         | WP#          | SI02        | SI02           |
| 24    | SPIHD         | HOLD#        | SI03        | SI03           |

**Footnote:**
1 SIO: Serial Data Input and Output

**Footer:**
Espressif Systems
ESP32-C6 Series Datasheet v1.4
Submit Documentation Feedback