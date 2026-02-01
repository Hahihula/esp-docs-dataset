**Title: Electrical Characteristics**

---

### Subtitle: Absolute Maximum Ratings

#### Section Title: 5.1 Absolute Maximum Ratings

Body Text:
Stresses above those listed in Table 5-1 *Absolute Maximum Ratings* may cause permanent damage to the device. These are stress ratings only and normal operation of the device at these or any other conditions beyond those indicated in Section 5.2 Recommended Operating Conditions is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

Table Title: Table 5-1. Absolute Maximum Ratings

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| Input power pins^1 | Allowed input voltage | -0.3 V | 3.6 V | |
| I_output^2 | Cumulative IO output current | — | 1.3 A | |
| T_STORE | Storage temperature | -40 °C | 150 °C | |

Footnotes:
1 For more information on input power pins, see Section *2.5.1 Power Pins*.
2 The product proved to be fully functional after all its IO pins were pulled high while being connected to ground for 24 consecutive hours at ambient temperature of 25 °C.

---

### Subtitle: Recommended Operating Conditions

#### Section Title: 5.2 Recommended Operating Conditions

Table Title: Table 5-2. Recommended Operating Conditions

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|----|-----|------|
| VDD3P3, VBAT, VDDA_PMU, VDDPST1, VDDPST2^2 | Recommended input voltage | 3.0 V | — | 3.6 V | |
| I_VDD | Cumulative input current^2 | - | 0.35 A | — | A |
| T_A | Ambient temperature | -40 °C | — | 105 °C | |

Footnotes:
1 See in conjunction with Section *2.5 Power Supply*.
2 If writing to eFuses, the voltage on its power supply pin VDDPST2 should not exceed 3.3 V as the circuits responsible for burning eFuses are sensitive to higher voltages.

---

### Subtitle: DC Characteristics (3.3 V, 25 °C)

#### Section Title: 5.3 DC Characteristics

Table Title: Table 5-3. DC Characteristics (3.3 V, 25 °C)

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|----|-----|------|
| C_IN^1 | Pin capacitance | — | 2 pF | - | pF |
| V_IH | High-level input voltage | (0.75 × VDD)^1 | – | VDD + 0.3 V | V |
| V_IL | Low-level input voltage | -0.3 V | – | 0.25 × VDD^1 | V |
| I_IH | High-level input current | — | – | 50 nA | nA |
| I_IL | Low-level input current | — | – | 50 nA | nA |

Footnotes:
1

---

**Footer:**
Espressif Systems
ESP32-H2 Series Datasheet v1.2
Submit Documentation Feedback