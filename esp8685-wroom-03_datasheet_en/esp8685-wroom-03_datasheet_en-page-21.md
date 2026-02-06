**Title: Electrical Characteristics**

---

### Subtitle: Absolute Maximum Ratings

#### Section Title: 6.1 Absolute Maximum Ratings

Stresses above those listed in Table 6-1 *Absolute Maximum Ratings* may cause permanent damage to the device. These are stress ratings only and functional operation of the device at these or any other conditions beyond those indicated under Table 6-2 Recommended Operating Conditions is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

**Table Title: Table 6-1. Absolute Maximum Ratings**

| Symbol | Parameter       | Min   | Max    | Unit |
|--------|-----------------|-------|--------|------|
| VDD33  | Power supply voltage | -0.3 | 3.6    | V    |
| T_STDBR| Storage temperature | -40   | 105    | °C   |

---

### Subtitle: Recommended Operating Conditions

#### Section Title: 6.2 Recommended Operating Conditions

**Table Title: Table 6-2. Recommended Operating Conditions**

| Symbol | Parameter       | Min   | Max    | Unit |
|--------|-----------------|-------|--------|------|
| VDD33  | Power supply voltage | 3.0  | 3.3    | V    |
| I_VDD  | Current delivered by external power supply | —     | A      |      |
| T_A    | Operating ambient temperature   | -40   | 105    | °C   |

---

### Subtitle: DC Characteristics (3.3 V, 25 °C)

#### Section Title: 6.3

**Table Title: Table 6-3. DC Characteristics (3.3 V, 25 °C)**

| Parameter       | Description                                    | Min     | Typ    | Max     | Unit |
|-----------------|-------------------------------------------------|---------|--------|---------|------|
| C_IN            | Pin capacitance                                 | —       |        |         | pF   |
| V_IH            | High-level input voltage                         | 0.75 × VDD¹ |    | VDD¹ + 0.3 | V |
| V_IL            | Low-level input voltage                          | -0.3   |        | —       | V    |
| I_IH            | High-level input current                           |         |        |         | nA   |
| I_IL            | Low-level input current                            |         |        |         | nA   |
| V_OH²           | High-level output voltage                        | 0.8 × VDD¹ |    | —       | V   |
| V VOL2          | Low-level output voltage                         |         |        | 0.1 × VDD¹ | V |
| IOH             | High-level source current (VDD¹ = 3.3 V, V_OH > 2.64 V, PAD_DRIVER = 3) | —       |    | 40     | mA   |
| IOL             | Low-level sink current (VDD¹ = 3.3 V, VOL = 0.495 V, PAD_DRVER = 3) |         |        | 28     | mA   |
| R PU            | Internal weak pull-up resistor                   | —       |    | 45     | kΩ   |
| R PD            | Internal weak pull-down resistor                 | —       |    | 45     | kΩ   |
| V_IH_n_RST      | Chip reset release voltage (CHIP_EN voltage within the specified range) | 0.75 × VDD¹ |    | VDD¹ + 0.3 | V |

---

**Footer:**
Espressif Systems
ESP8685-WROOM-03 Datasheet v1.5

Submit Documentation Feedback