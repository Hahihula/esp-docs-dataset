**Title: Electrical Characteristics**

---

### Section 61 Absolute Maximum Ratings

Stresses above those listed in Table **6-1 Absolute Maximum Ratings** may cause permanent damage to the device. These are stress ratings only and functional operation of the device at these or any other conditions beyond those indicated under Table **6-2 Recommended Operating Conditions** is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

---

#### Table 6-1: Absolute Maximum Ratings

| Symbol | Parameter       | Min   | Max    | Unit |
|--------|-----------------|-------|--------|------|
| VDD33  | Power supply voltage | -0.3 | 3.6    | V    |
| TSTORe | Storage temperature | -40   | 105 °C | °C   |

---

### Section 62 Recommended Operating Conditions

#### Table 6-2: Recommended Operating Conditions

| Symbol | Parameter       | Min   | Max    | Unit |
|--------|-----------------|-------|--------|------|
| VDD33  | Power supply voltage | 3.0  | 3.3    | V    |
| IVDD   | Current delivered by external power supply | —     | A      |      |
| TA     | Operating ambient temperature (85 °C version) | -40   | 85 °C | °C   |

---

### Section 63 DC Characteristics (3.3 V, 25 °C)

#### Table 6-3: DC Characteristics

| Parameter       | Description                           | Min    | Typ     | Max    | Unit |
|-----------------|---------------------------------------|--------|---------|--------|------|
| CIN             | Pin capacitance                       | —      | 2       | —      | pF   |
| VIH             | High-level input voltage               | 0.75 × VDD^1 | —    | V     |
| VIL             | Low-level input voltage                | -0.3   | —       | 0.25 × VDD^1 | V |
| ILH             | High-level input current               | —      | 50 nA  | —      | nA   |
| IIL             | Low-level input current                | —      | 50 nA  | —      | nA   |
| VOH^2           | High-level output voltage              | 0.8 × VDD^1 | —    | V     |
| VOL^2           | Low-level output voltage               | —      | 0.1 × VDD^1 | V     |
| IOH             | High-level source current (VDD = 3.3 V, VOH >= 2.64 V, PAD_DRIVER = 3) | 40    | mA     | —     |
| IOL             | Low-level sink current (VDD = 3.3 V, VOI = 0.495 V, PAD_DRV = 3) | -      | 28 mA  | —     |
| RPu             | Internal weak pull-up resistor         |        | 45 kΩ   |       | kΩ   |
| RPD             | Internal weak pull-down resistor       |        | 45 kΩ   |       | kΩ   |
| VIH_nRST        | Chip reset release voltage CHIP_EN voltage within the specified range (0.75 × VDD^1) | —     | - VDD^1 + 0.3 | V |

---

*Espressif Systems*

**Page Number: 22**

**Document Title:** ESP32-C3-WROOM-02 & WROOM-02U Datasheet v1.6

**Submit Documentation Feedback**