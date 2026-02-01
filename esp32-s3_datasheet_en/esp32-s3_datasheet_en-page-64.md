Title: Electrical Characteristics

Subtitle: Absolute Maximum Ratings (Section 5.1)

Body Text:
Stresses above those listed in Table 5-1 *Absolute Maximum Ratings* may cause permanent damage to the device. These are stress ratings only and normal operation of the device at these or any other conditions beyond those indicated in Section 5.2 Recommended Operating Conditions is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

Table:
- **Title**: Table 5-1. Absolute Maximum Ratings
- Columns: Parameter, Description, Min, Max, Unit

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| Input power pins¹ | Allowed input voltage | -0.3 V | 3.6 V | |
| I_output² | Cumulative IO output current | — | 1500 mA | |
| T_STORE³ | Storage temperature | -40 °C | 150 °C | |

Footnotes:
¹ For more information on input power pins, see Section *2.5.1 Power Pins*.
² The product proved to be fully functional after all its IO pins were pulled high while being connected to ground for 24 consecutive hours at ambient temperature of 25 °C.

Subtitle: Recommended Operating Conditions (Section 5.2)

Body Text:
For recommended ambient temperature, see Section *1 ESP32-S3 Series Comparison*.

Table:
- **Title**: Table 5-2. Recommended Operating Conditions
- Columns: Parameter, Description, Min, Typ, Max, Unit

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|----|-----|------|
| VDDA, VDD3P3 | Recommended input voltage | 3.0 V | — | 3.6 V | V |
| VDD3P3_RTC⁴² | Recommended input voltage | 3.0 V | 3.3 V | 3.6 V | V |
| VDD_SPI (as input)³ | - | 1.8 V | 3.3 V | 3.6 V | V |
| VDD3P3_CPU⁴³ | Recommended input voltage | 3.0 V | — | 3.6 V | V |
| I_VDD⁵⁴ | Cumulative input current | - | 0.5 A | — | A |

Footnotes:
¹ See in conjunction with Section *2.5 Power Supply*.
² If VDD3P3_RTC is used to power VDD_SPI (see Section *2.5.2 Power Scheme*), the voltage drop on R_SPI should be accounted for. See also Section *5.3 VDD_SPI Output Characteristics*.
³ If writing to eFuses, the voltage on VDD3P3_CPU should not exceed 3.3 V as the circuits responsible for burning eFuses are sensitive to higher voltages.

⁴ If you use a single power supply, the recommended output current is 500 mA or more.

Footer:
- Company: Espressif Systems
- Document Version and Submission Information: ESP32-S3 Series Datasheet v2.1 | Submit Documentation Feedback

Page Number: 64