**Title:**
2 Pins

**Subtitle:**
2.5 Power Supply

**Subsection Title:**
2.5.1 Power Pins

**Body Text:**
The chip is powered via the power pins described in Table 2-9 Power Pins.

**Table Header (Table 2-9):**
- QFN48
- Pin No.
- Name
- Direction
- Power Domain/Other
- IO Pins

**Table Content:**

| Pin No. | Name       | Direction | Power Domain/Other                   | IO Pins |
|---------|-----------|-----------|--------------------------------------|---------|
| 1       | VDDA6     | Input     | Analog power domain 3.3 V            |         |
| 2       | GND        | —         | External ground connection           |         |
| 3       | VDDA7     | Input     | Analog power domain 3.3 V            |         |
| 6       | VDDA8     | Input     | Analog power domain 3.3 V            |         |
| 8       | VDDPST1   | Input     | LP digital power domain               | LP IO   |
| 24      | VDDPST2   | Input     | HP digital and part of analog pin power domains | HP IO |
| 29      | VDD_SPI^3 | Output    | Off-package flash                    | Flash IO|
| 39      | VDDPST3   | Input     | HP digital power domain               | HP IO   |
| 40      | VDDA1     | Input     | Analog power domain 3.3 V            |         |
| 41      | VDDA2     | Input     | Analog power domain 3.3 V            |         |
| 43      | GND        | —         | External ground connection           |         |
| 44      | VDDA3     | Input     | Analog power domain 3.3 V            |         |
| 45      | VDDA4     | Input     | Analog power domain 3.3 V            |         |
| 46      | VDDA5     | Input     | Analog power domain 3.3 V            |         |
| 47      | GND        | —         | External ground connection           |         |

**Footnotes:**
1 See in conjunction with Section 2.5.2 Power Scheme.
2 For recommended and maximum voltage and current, see Section 5.1 Absolute Maximum Ratings and Section 5.2 Recommended Power Supply Characteristics.
3 To configure VDD_SPI as input or output, see ESP32-C5 Technical Reference Manual > Chapter Low-Power Management.
4 LP IO pins are those powered by VDDPST1 and so on, as shown in Figure 2-2 ESP32-C5 Power Scheme. See also Table 2-1 Pin Overview > Column Pin Providing Power.

**Subsection Title:**
2.5.2 Power Scheme

**Body Text:**
The power scheme is shown in Figure 2-2 ESP32-C5 Power Scheme.
The components on the chip are powered via voltage regulators.

**Table Header (Table 2-10):**
- Voltage Regulator
- Output
- Power Supply

**Table Content:**

| Voltage Regulator | Output | Power Supply |
|-------------------|--------|--------------|
| HP                | 1.1 V  | HP power domain |
| LP                | 1.1 V  | LP power domain |

**Footer Text:**
Espressif Systems
Submit Documentation Feedback

**Document Information:**
ESP32-C5 Series Datasheet v1.0