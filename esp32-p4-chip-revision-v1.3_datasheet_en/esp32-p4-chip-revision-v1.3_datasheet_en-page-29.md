**Title:**
2.6 Power Supply

**Subtitle:**
2.6.1 Power Pins

**Body Text:**
The chip is powered via the power pins described in Table 2-11 Pin Power Pins.

**Table Title:**
Table 2-11. Power Pins

| Pin No. | Name       | Direction | Power Domain / Other | IO Pins |
|---------|-----------|-----------|----------------------|---------|
| 9       | VDD_LP    | Input     | LP power domain      |         |
| 21      | VDD_IO_0  | Input     | Digital power domain | HP IO   |
| 26      | VDD_HP_0  | Input     | Digital power domain |         |
| 30      | VDD_FLASHIO^2 | Input    | Flash                | flash IO|
| 41      | VDD_MIPI_DPHY | Input   | MIPI PHY            | MIPI IO|
| 51      | VDD_USBPHY | Input     | USB PHY             | High-speed USB IO |
| 59      | VDD_PSRAM_0 | Input    | PSRAM               | PSRAM IO|
| 62      | VDD_IO_4  | Input     | Digital power domain | HP IO   |
| 67      | VDD_PSRAM_1 | Input    | PSRAM               | PSRAM IO|
| 71      | VDDO_FLASH | Output    | Off-package flash, output 50 mA current at the maximum |         |
| 72      | VDDO_PSRAM | Output    | In-package and off-package PSRAM, output 50 mA current at the maximum |         |
| 73      | VDDO_3    | Output    | Output 50 mA current at the maximum |         |
| 74      | VDDO_4    | Output    | Output 50 mA current at the maximum |         |
| 75      | VDD_LDO   | Input     | Analog power domain, providing power for LDOs |         |
| 76      | VDD_HP_2  | Input     | Digital power domain |         |
| 77      | VDD_DCDC   | Input     | Analog power domain, providing power for DC/DC control |         |
| 85      | VDD_IO_5  | Input     | Digital power domain | HP IO   |
| 91      | VDD_HP_3  | Input     | Digital power domain |         |
| 96      | VDD_IO_6  | Input     | Digital power domain | HP IO   |
| 101     | VDD_ANA   | Input     | Analog power domain |         |
| 102     | VDD_BAT   | Input     | Analog power domain, connecting to external batteries optionally |         |
| 105     | GND       |           | External ground connection |         |

**Footnotes:**
^1 See in conjunction with Section 2.6.2 Power Scheme.
^2 VDD_FLASHIO provides power for flash IO, and the voltage should be adjusted according to the specific flash model.

In this document, all related descriptions are based on a 3.3 V flash as an example.

For recommended and maximum voltage and current, see Section 5.1 Absolute Maximum Ratings and Section 5.2 Recommended Operating Conditions.
^4 LP IO pins are those powered by VDD_LP or VDD_BAT, as shown in Figure 2-2 ESP32-P4 Power Scheme. See also Table 2-1 Pin Overview > Column Pin Providing Power.

**Subsection Title:**
2.6.2 Power Scheme

**Body Text:**
The power scheme is shown in Figure 2-2 ESP32-P4 Power Scheme.
The components on the chip are powered via voltage regulators.

**Footer Information:**
Espressif Systems
Submit Documentation Feedback
ESP32-P4 Series Datasheet v0.6