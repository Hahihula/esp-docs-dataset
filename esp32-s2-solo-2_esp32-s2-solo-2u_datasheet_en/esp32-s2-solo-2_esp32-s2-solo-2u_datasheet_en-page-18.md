**Title: Electrical Characteristics**

---

### Subtitle: Absolute Maximum Ratings

#### Section Title: 5.1 Absolute Maximum Ratings

Stresses above those listed in Table 5-1 *Absolute Maximum Ratings* may cause permanent damage to the device. These are stress ratings only and functional operation of the device at these or any other conditions beyond those indicated under Table 5-2 Recommended Operating Conditions is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

**Table Title: Table 5-1. Absolute Maximum Ratings**

| Symbol | Parameter           | Min   | Max    | Unit |
|--------|---------------------|-------|--------|------|
| VDD33  | Power supply voltage | -0.3 | 3.6    | V    |
| TSTORe | Storage temperature  | -40   | 105    | °C   |

---

### Subtitle: Recommended Operating Conditions

#### Section Title: 5.2 Recommended Operating Conditions

**Table Title: Table 5-2. Recommended Operating Conditions**

| Symbol | Parameter           | Min   | Max    | Unit |
|--------|---------------------|-------|--------|------|
| VDD33  | Power supply voltage | 3.0   | 3.6    | V    |
| IVDD   | Current delivered by external power supply | —     | A      |      |
| TA     | Operating ambient temperature (85 °C version) | -40   | 85     | °C   |

---

### Subtitle: DC Characteristics

#### Section Title: 5.3 DC Characteristics (3.3 V, 25 °C)

**Table Title: Table 5-3. DC Characteristics (3.3 V, 25 °C)**

| Parameter       | Description                                    | Min   | Max    | Unit |
|-----------------|-----------------------------------------------|-------|--------|------|
| CIN             | Pin capacitance                               | —     | 2      | pF   |
| VIH             | High-level input voltage                        | 0.75 × VDD^1 | —       | V    |
| VIL             | Low-level input voltage                         | -0.3  | —      | V    |
| IL              | High-level input current                         | —     | 50     | nA   |
| ILL             | Low-level input current                          | —     | 50     | nA   |
| VOH^2           | High-level output voltage                       | 0.8 × VDD^1 | —       | V    |
| VOL^2           | Low-level output voltage                        | —     | 0.1 × VDD^1 | V    |
| IOH             | High-level source current (VDD = 3.3 V, VOH >= 2.64 V, PAD_DRIVER = 3) | 40   | —      | mA   |
| IOL             | Low-level sink current (VDD = 3.3 V, VOH = 0.495 V, PAD_DRVER = 3) | -     | 28    | mA   |
| RPu             | Internal weak pull-up resistor                  | —     | 45     | kΩ   |
| RPD             | Internal weak pull-down resistor                | —     | 45     | kΩ   |
| VIH_nRST        | Chip reset release voltage (CHIP PU voltage within the specified range) | 0.75 × VDD^1 + 0.3 | -    | V    |

---

**Footer:**
- Page number: 18
- Document version and feedback link:
  - ESP32-S2-SOLO-2 & SOLO-2U Datasheet v1.3
  - Submit Documentation Feedback