**Title: Electrical Characteristics**

The values presented in this section are preliminary and may change with the final release of this datasheet.

---

**Subtitle: Absolute Maximum Ratings (Section 6.1)**

Stresses above those listed in Table **6-1 Absolute Maximum Ratings** may cause permanent damage to the device. These are stress ratings only, functional operation of the device at these or any other conditions beyond those indicated under Table **6-2 Recommended Operating Conditions** is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

| Symbol | Parameter           | Min  | Max   | Unit |
|--------|---------------------|------|-------|------|
| VDD33  | Power supply voltage | -0.3 | 3.6   | V    |
| T_STDBORE | Storage temperature | -40  | 85    | °C   |

**Subtitle: Recommended Operating Conditions (Section 6.2)**

Table **6-2 Recommended Operating Conditions**

| Symbol | Parameter           | Min  | Typ  | Max   | Unit |
|--------|---------------------|------|------|-------|------|
| VDD33  | Power supply voltage | 3.0  | 3.3  | 3.6   | V    |
| I_VDD  | Current delivered by external power supply | —     | —    | A     |      |
| T_A    | Operation ambient temperature | -40  | —    | 85 °C |      |

**Subtitle: DC Characteristics (Section 6.3)**

Table **6-3 DC Characteristics (3.3 V, 25 °C)**

| Parameter       | Description                           | Min   | Typ  | Max   | Unit |
|-----------------|---------------------------------------|-------|------|-------|------|
| C_IN            | Pin capacitance                       | —     | 2    | —     | pF   |
| V_IH            | High-level input voltage               | 0.75 × VDD¹ | — | VDD¹ + 0.3 | V |
| V_IL            | Low-level input voltage                | -0.3  | —    | 0.25 × VDD¹ | V |
| I_IH            | High-level input current               | —     |      | 50 nA |      |
| I_IL            | Low-level input current                | —     |      | 50 nA |      |
| V_OH²           | High-level output voltage              | 0.8 × VDD¹ | — | V    |      |
| V VOL2          | Low-level output voltage               | —     | —    | 0.1 × VDD¹ | V |
| I_OH            | High-level source current (VDD¹ = 3.3 V, V VOL² >= 2.64 V, PAD_DRIVER = 3) | —     |      | 40   | mA   |
| I_OL            | Low-level sink current (VDD¹ = 3.3 V, V VOL² = 0.495 V, PAD_DRV = 3) | -       |    | 28   | mA   |
| R PU            | Internal weak pull-up resistor         | —     |      | 45 kΩ |      |

**Footer:**

Espressif Systems  
Submit Documentation Feedback

ESP32-C5-MINI-1 Datasheet v1.0
Page number at the bottom of page is "29".