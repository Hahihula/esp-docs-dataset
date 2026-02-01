**Title:**
5 Electrical Characteristics

**Note:** The values presented in this section are preliminary and may change with the final release of this datasheet.

---

**Subtitle: 5.1 Absolute Maximum Ratings**

**Body Text:**
Stresses above those listed in Table **5-1 Absolute Maximum Ratings** may cause permanent damage to the device. These are stress ratings only, normal operation of the device at these or any other conditions beyond those indicated in Section **5.2 Recommended Operating Conditions** is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

---

**Table 5-1: Absolute Maximum Ratings**

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| VDD_LDO, VDD_DCDC, VDD_ANA, VDD_BAT, VDD_LP | Allowed input voltage | -0.3 | 3.6 | V |
| VDD_IO_0, VDD_FLASHIO³, VDD_IO_4, VDD_IO_5, VDD_IO_6 | Allowed input voltage | 1.62/–0.3 | 1.98/3.6 | V |
| VDD_PSRAM_0, VDD_PSRAM_1 | Allowed input voltage | - | 1.98 | V |
| VDD_HP_0, VDD_HP_2, VDD_HP_3 | Allowed input voltage | 0 | 1.3 | V |
| VDD_MIPI_DPHY | Allowed input voltage | 0 | 2.75 | V |
| VDD_USBPHY | Allowed input voltage | -0.66 | 3.96 | V |
| I_output² | Cumulative IO output current | — | 1500 mA |
| T_store | Storage temperature | –40 | 150 °C |

**Footnotes:**
¹ For more information on input power pins, see Section **2.6.1 Power Pins**.
² The product proved to be fully functional after all its IO pins were pulled high while being connected to ground for 24 consecutive hours at ambient temperature of 25 °C.

³ VDD_FLASHIO provides power for flash IO, and the voltage should be adjusted according to the specific flash model.

---

**Subtitle: 5.2 Recommended Operating Conditions**

**Table 5-2: Recommended Operating Conditions**

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| VDD_LDO, VDD_DCDC, VDD_ANA, VDD_LP, VDD_BAT | Recommended input voltage | -3.0/–3.3 | 3.6 / 3.5 | V |
| VDD_IO_0, VDD_FLASHIO, VDD_IO_4, VDD_IO_5, VDD_IO_6 | Recommended input voltage | — | 1.98/3.6 | V |
| VDD_PSRAM_0, VDD_PSRAM_1 | Recommended input voltage | - | 1.95 | V |
| VDD_HP_0, VDD_HP_2, VDD_HP_3¹ | Recommended input voltage | — | 1.1 / 1.3 | V |

**Footnote:**
¹ Cont’d on next page

---

**Footer:** 
Espressif Systems  
80  
ESP32-P4 Series Datasheet v0.6  

Submit Documentation Feedback