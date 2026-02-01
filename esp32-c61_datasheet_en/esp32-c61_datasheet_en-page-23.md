**Title:**
2.5 Power Supply

**Subtitle:**
2.5.1 Power Pins

**Body Text:**
The chip is powered via the power pins described in Table 2-8 Power Pins.

**Table Title:**
Table 2-8. Power Pins

| Pin No. | Pin Name | Direction | Power Domain / Other | IO Pins |
|---------|----------|-----------|----------------------|---------|
| 2       | VDDA3    | Input     | Analog power domain  |         |
| 3       | VDDA4    | Input     | Analog power domain  |         |
| 5       | VDDPST1  | Input     | HP digital and part of LP digital power domains | LP IO   |
| 23      | VDD_SPI  | Output    | A power supply from VDDPST2 used to power the flash |        |
| 30      | VDDPST2  | Input     | HP digital power domain | HP IO  |
| 37      | VDDA1    | Input     | Analog power domain   |         |
| 40      | VDDA2    | Input     | Analog power domain   |         |
| 41      | GND      | —         | External ground connection |        |

**Footnotes:**
1. See in conjunction with Section 2.5.2 Power Scheme.
2. For recommended and maximum voltage, see Section 5.1 Absolute Maximum Ratings and Section 5.2 Recommended Operating Conditions.

3. LP IO pins are those powered by VDDPST1 and so on, as shown in Figure 2-2 ESP32-C61 Power Scheme. See also Table 2-1 Pin Overview > Column Pin Providing Powerer.

**Subsection Title:**
2.5.2 Power Scheme

**Body Text:**
The power scheme is shown in Figure 2-2 ESP32-C61 Power Scheme.
The components on the chip are powered via voltage regulators.

**Table Title:**
Table 2-9. Voltage Regulators

| Voltage Regulator | Output    | Power Supply |
|-------------------|-----------|-------------|
| HP                |           | 1.1 V       | HP power domain |
| LP                |           | 1.1 V       | LP power domain |

**Footer:**
Espressif Systems
23 ESP32-C61 Series Datasheet v0.5