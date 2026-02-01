**Title:**
5 Electrical Characteristics

**Note:** 
The values presented in this section are preliminary and may change with the final release of this datasheet.

---

**Subtitle: 5.1 Absolute Maximum Ratings**

Body Text:
Stresses above those listed in Table **5-1 Absolute Maximum Ratings** may cause permanent damage to the device. These are stress ratings only normal operation of the device at these or any other conditions beyond those indicated in Section **5.2 Recommended Operating Conditions** is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

**Table 5-1: Absolute Maximum Ratings**

| Parameter       | Description                | Min   | Max    | Unit |
|-----------------|-----------------------------|-------|--------|------|
| Input power pins^1 | Allowed input voltage      | -0.3  | 3.6 V  |      |
| I_output^2      | Cumulative IO output current| —     | 1500 mA|      |
| T_STORE         | Storage temperature        | -40   | 150 °C |      |

Footnotes:
1 For more information on input power pins, see Section **2.5 Power Pins**.
2 The product proved to be fully functional after all its IO pins were pulled high while being connected to ground for 24 consecutive hours at ambient temperature of 25 °C.

---

**Subtitle: 5.2 Recommended Operating Conditions**

Body Text:
Table **5-2. Recommended Operating Conditions**

| Parameter^1 | Description                | Min   | Max    | Unit |
|-------------|-----------------------------|-------|--------|------|
| VDDA1, VDDA2, VDDAP3P3  | Recommended input voltage  | 3.0   | 3.6 V  |      |
| VDDPST1     | Recommended input voltage  | 3.0   | 3.6 V  |      |
| VDD_SPI (as input)       | —                            | 1.8   | 3.6 V  |      |
| VDDPST2^2,3 | Recommended input voltage  | 3.0   | 3.6 V  |      |
| I_VDD        | Cumulative input current    | 0.5   | — A    |      |

Footnotes:
1 See in conjunction with Section **2.5 Power Supply**.
2 If VDDPST2 is used to power VDD_SPI (see Section **2.5.2 Power Scheme**), the voltage drop on R_SPI should be accounted for.
3 If writing to eFuses, the voltage on VDDPST2 should not exceed 3.3 V as the circuits responsible for burning eFuses are sensitive to higher voltages.

---

**Footer:**
Espressif Systems
Page number: 55

ESP32-C61 Series Datasheet v0.5