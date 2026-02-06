**Title: Electrical Characteristics**

---

### Subtitle: Absolute Maximum Ratings

#### Section Title: 6.1 Absolute Maximum Ratings

Stresses above those listed in Table 6-1 *Absolute Maximum Ratings* may cause permanent damage to the device. These are stress ratings only and functional operation of the device at these or any other conditions beyond those indicated under Table 6-2 Recommended Operating Conditions is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

**Table Title: Table 6-1. Absolute Maximum Ratings**

| Symbol | Parameter       | Min   | Max    | Unit |
|--------|-----------------|-------|--------|------|
| VDD33  | Power supply voltage | -0.3 | 3.6    | V    |
| T_STDBR| Storage temperature | -40   | 105 °C| °C   |

---

### Subtitle: Recommended Operating Conditions

#### Section Title: 6.2 Recommended Operating Conditions

**Table Title: Table 6-2. Recommended Operating Conditions**

| Symbol | Parameter       | Min   | Max    | Unit |
|--------|-----------------|-------|--------|------|
| VDD33  | Power supply voltage | 3.0  | 3.3    | V    |
| I_VDD  | Current delivered by external power supply | -     | —      | A    |
| T_A    | Operating ambient temperature   | -40   | 105 °C| °C   |

---

### Subtitle: DC Characteristics (3.3 V, 25 °C)

#### Section Title: 6.3 DC Characteristics

**Table Title: Table 6-3. DC Characteristics**

| Parameter       | Description                                    | Min    | Max     | Unit |
|-----------------|------------------------------------------------|--------|---------|------|
| C_IN            | Pin capacitance                                | —      | 2       | pF   |
| V_IH            | High-level input voltage                        | (0.75 × VDD)¹ | (VDD + 0.3)¹ | V    |
| V_IL            | Low-level input voltage                         | -0.3   | —       | V    |
| I_IH            | High-level input current                         | —      | 50 nA  | mA   |
| I_IL            | Low-level input current                          | —      | 50 nA  | mA   |
| V_OH²           | High-level output voltage                       | (0.8 × VDD)¹ | V    |
| V VOL           | Low-level source current (VDD = 3.3 V, IOH > 2.64 V, PAD_DRIVER = 3) | —      | 40 mA  | mA   |
| I_OH            | High-level sink current (VDD = 3.3 V, VOL = 0.495 V, PAD_DRV = 3) | -     | 28 mA  | mA   |
| R_PU            | Internal weak pull-up resistor                   | —      | 45 kΩ  | Ω    |
| R_PD            | Internal weak pull-down resistor                 | —      | 45 kΩ  | Ω    |
| V_IH_n_RST       | Chip reset release voltage (CHIP_EN voltage within the specified range) | (0.75 × VDD)¹ | (VDD + 0.3)¹ | V   |

---

*Footnotes:*
1. VDD = power supply
2. VOL = output

**Footer:**  
Espressif Systems  
ESP8685-WROOM-01 Datasheet v1.5  
Submit Documentation Feedback