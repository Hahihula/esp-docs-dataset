**Title: Electrical Characteristics**

---

### Subtitle: Absolute Maximum Ratings

#### Section Title: 5.1 Absolute Maximum Ratings

Body Text:
Stresses above those listed in Table 5-1 *Absolute Maximum Ratings* may cause permanent damage to the device. These are stress ratings only and normal operation of the device at these or any other conditions beyond those indicated in Section 5.2 Recommended Operating Conditions is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

---

**Table Title: Table 5-1. Absolute Maximum Ratings**

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| Input power pins^1 | Allowed input voltage | -0.3 V | 3.6 V |      |
| I_output^2 | Cumulative IO output current | — | 1800 mA |      |
| T_STORE | Storage temperature | -40 °C | 150 °C |      |

Footnotes:
1 For more information on input power pins, see Section **2.5.1 Power Pins**.
2 The product proved to be fully functional after all its IO pins were pulled high while being connected to ground for 24 consecutive hours at ambient temperature of 25 °C.

---

### Subtitle: Recommended Operating Conditions

#### Section Title: 5.2 Recommended Operating Conditions

Body Text:
For recommended ambient temperature, see Section **ESP32-S2 Series Comparison**.

---

**Table Title: Table 5-2. Recommended Operating Conditions**

| Parameter^1 | Description | Min | Typ | Max | Unit |
|-------------|-------------|-----|-----|-----|------|
| VDDA, VDD3P3, VDD3P3_RTC | Recommended input voltage | — |     |     |      |
| VDD3P3_RTC_IO^2 | Recommended input voltage | 3.0 V | 3.6 V |       |      |
| VDD_SPI (as input) |         |    |     |     |      |
| VDD3P3_CPU^3 | Recommended input voltage | — | 3.6 V |       |      |
| I_VDD | Cumulative input current | 0.5 A | — | — | A   |
| T_j | Junction temperature | -40 °C | 125 °C |     | °C  |

Footnotes:
1 See in conjunction with Section **2.5 Power Supply**.
2 If VDD3P3_RTC_IO is used to power VDD_SPI (see Section **2.5.2 Power Scheme**), the voltage drop on R_SPI should be accounted for. See also Section *5.3 VDD_SPI Output Characteristics*.
3 If writing to eFuses, the voltage on VDD3P3_CPU should not exceed 3.3 V as the circuits responsible for burning eFuses are sensitive to higher voltages.

---

**Footer:**
Espressif Systems  
48  
ESP32-S2 Series Datasheet v1.8

[Submit Documentation Feedback](#)