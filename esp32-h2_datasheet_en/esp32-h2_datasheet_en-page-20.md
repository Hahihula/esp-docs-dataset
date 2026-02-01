**Title:**
2.5 Power Supply

**Subtitle:**
2.5.1 Power Pins

**Body Text:**
The chip is powered via the power pins described in Table 2-7.

**Table Title:**
Table 2-7. Power Pins

| Pin No. | Pin Name       | Direction    | Power Domain/Other IO Pins |
|---------|---------------|--------------|---------------------------|
| 1       | VDD3P3        | Input        | Analog power domain       |
| 2       | VDD3P3        | Input        | Analog power domain       |
| 9       | VDDPST1       | Input        | IO power domain           | Digital IO, LP IO^3 |
| 18      | VBAT          | Input        | Analog power domain or battery power supply | GPIO12, XTAL_32K_P, XTAL_32K_N |
| 19      | VDDA_PMU      | Input        | Analog power domain       | GPIO12, XTAL_32K_P, XTAL_32K_N |
| 20      | VDDPST2       | Input        | No power domain           | Digital IO |
| 27      | VDD3P3        | Input        | Analog power domain       |
| 33      | GND           | -            | External ground connection|

**Footnotes:**
1. See in conjunction with Section 2.5.2 Power Scheme.
2. For recommended and maximum voltage and current, see Section 5.1 Absolute Maximum Ratings and Section 5.2 Recommended Operating Conditions.
3. For the classification of digital IO and LP IO, see Section 2.2 Pin Overview.

**Subsection Title:**
2.5.2 Power Scheme

**Body Text:**
The power scheme is shown in Figure 2-2 ESP32-H2 Power Scheme.

The components on the chip are powered via voltage regulators.
  
**Table Title:**
Table 2-8. Voltage Regulators

| Voltage Regulator | Output    | Power Supply |
|-------------------|-----------|-------------|
|                   | Digital   | 1.1 V       | Digital power domain |
|                   | Low-power | 1.1 V       | LP power domain |

**Footer:**
Espressif Systems
ESP32-H2 Series Datasheet v1.2

Submit Documentation Feedback