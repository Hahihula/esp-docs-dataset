**Title: Electrical Characteristics**

---

### Subtitle: Absolute Maximum Ratings

#### Section Title: 6.1 Absolute Maximum Ratings

Stresses above those listed in Table 6-1 *Absolute Maximum Ratings* may cause permanent damage to the device. These are stress ratings only and functional operation of the device at these or any other conditions beyond those indicated under Table 6-2 *Recommended Operating Conditions* is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

**Table Title: Table 6-1. Absolute Maximum Ratings**

| Symbol | Parameter           | Min   | Max    | Unit |
|--------|---------------------|-------|--------|------|
| VDD33  | Power supply voltage | -0.3 | 3.6    | V    |
| TSTOR  | Storage temperature  | -40   | 105 °C | °C   |

---

### Subtitle: Recommended Operating Conditions

#### Section Title: 6.2 Recommended Operating Conditions

**Table Title: Table 6-2. Recommended Operating Conditions**

| Symbol | Parameter           | Min    | Max     | Unit |
|--------|---------------------|--------|---------|------|
| VDD33  | Power supply voltage | 3.0   | 3.3     | V    |
| IVDD   | Current delivered by external power supply | —      | A       |      |
| TA     | Operating ambient temperature (85 °C version) | -40   | 85 °C  | °C   |

---

### Subtitle: DC Characteristics

#### Section Title: 6.3 DC Characteristics (3.3 V, 25 °C)

**Table Title: Table 6-3. DC Characteristics (3.3 V, 25 °C)**

| Parameter       | Description                   | Min    | Max     | Unit |
|-----------------|-------------------------------|--------|---------|------|
| CIN             | Pin capacitance               | —      | 2       | pF   |
| VIH             | High-level input voltage      | 0.75 × VDD^1 | — | V    |
| VIL             | Low-level input voltage       | -0.3   | —       | V    |
| IL              | High-level input current      | —      | 50 nA  | mA   |
| ILL             | Low-level input current       | —      | 50 nA  | mA   |
| VOH^2           | High-level output voltage     | 0.8 × VDD^1 | — | V    |
| VOL^2           | Low-level output voltage      | —      | 0.1 × VDD^1 | V    |
| IOH             | High-level source current (VDD = 3.3 V, VOH >= 2.64 V, PAD_DRIVER = 3) | 40   | mA     |      |
| IOL             | Low-level sink current (VDD = 3.3 V, VOI = 0.495 V, PAD_DRV = 3) | —    | 28     | mA   |
| RPu             | Internal weak pull-up resistor | 45   | kΩ      |      |
| RPD             | Internal weak pull-down resistor | 45   | kΩ      |      |
| VIH_nRST        | Chip reset release voltage CHIP_EN voltage within the specified range (0.75 × VDD^1) | —    | VDD + 0.3 | V |

---

**Footer:**
Espressif Systems
22 ESP32-C3-MINI-1 & MINI-1U Datasheet v2.1

Submit Documentation Feedback