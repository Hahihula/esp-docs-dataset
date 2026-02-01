Title: Electrical Characteristics

Subtitle: Absolute Maximum Ratings (Section 5.1)

Body Text:
Stresses above those listed in Table 5-1 *Absolute Maximum Ratings* may cause permanent damage to the device. These are stress ratings only and normal operation of the device at these or any other conditions beyond those indicated in Section 5.2 Recommended Operating Conditions is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

Table Title: Table 5-1. Absolute Maximum Ratings

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| Input power pins^1 | Allowed input voltage | -0.3 V | 3.6 V | |
| I\(_{output}^{2}\) | Cumulative IO output current | — | 1000 mA | |
| T\(_{STORE}\) | Storage temperature | -40 °C | 150 °C | |

Footnotes:
^1 For more information on input power pins, see Section *2.5.1 Power Pins*.
^2 The product proved to be fully functional after all its IO pins were pulled high while being connected to ground for 24 consecutive hours at ambient temperature of 25 °C.

Subtitle: Recommended Operating Conditions (Section 5.2)

Table Title: Table 5-2. Recommended Operating Conditions

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| VDDA1, VDDA2, VDDA3P3 | Recommended input voltage | 3.0 V | 3.6 V | — |
| VDDPST1 | Recommended input voltage | 3.0 V | 3.6 V | — |
| VDD_SPI (as input) | - | 3.0 V | 3.6 V | — |
| VDDPST2,^3 | Recommended input voltage | 3.0 V | 3.6 V | — |
| I\(_{VDD}\) | Cumulative input current | 0.5 A | - | |
| T\(_{A}\) | Ambient temperature | -40 °C | 105 °C | |

Footnotes:
^1 See in conjunction with Section *2.5 Power Supply*.
^2 If VDDPST2 is used to power VDD_SPI (see Section *2.5.2 Power Scheme*), the voltage drop on R\(_{SP1}\) should be accounted for. See also Section *5.3 VDD_SPI Output Characteristics*.
^3 If writing to eFuses, the voltage on VDDPST2 should not exceed 3.3 V as the circuits responsible for burning eFuses are sensitive to higher voltages.

Footer:
Espressif Systems
Page Number: 64

Link Texts:
- Submit Documentation Feedback (at the bottom of the page)