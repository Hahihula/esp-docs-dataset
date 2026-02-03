**Title: Electrical Characteristics**

---

### Subtitle: Absolute Maximum Ratings

#### Section Title: 5.1 Absolute Maximum Ratings

Stresses above those listed in Table 5-1 *Absolute Maximum Ratings* may cause permanent damage to the device. These are stress ratings only and normal operation of the device at these or any other conditions beyond those indicated in Section 5.2 Recommended Power Supply Characteristics is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

**Table Title: Table 5-1. Absolute Maximum Ratings**

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| VDDA, VDD3P3, VDD3P3_RTC, VDD3P3_CPU, VDD_SDIO | Allowed input voltage | -0.3 | 3.6 | V |
| \[output\]¹ | Cumulative IO output current | — | **1200** mA | |
| T STORE | Storage temperature | -40 | 150 | °C |

Footnote:
¹ The product proved to be fully functional after all its I/O pins were pulled high while being connected to ground for 24 consecutive hours at ambient temperature of 25 °C.

---

### Subtitle: Recommended Power Supply Characteristics

#### Section Title: 5.2 Recommended Power Supply Characteristics

**Table Title: Table 5-2. Recommended Power Supply Characteristics**

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|----|-----|------|
| VDDA, VDD3P3_RTC, VDD3P3, VDD_SDIO (3.3 V mode)¹ note 1 | Voltage applied to power supply pins per power domain | **2.3/3.0** note 2 | 3.3 | 3.6 | V |
| VDD3P3_CPU | Voltage applied to power supply pin | 1.8 | — | 3.3 | V |
| I VDD | Current delivered by external power supply | **0.5**— | — | A |
| T note 3 | Operating temperature | -40 | – | 125 | °C |

Footnotes:
¹ VDD_SDIO works as the power supply for the related IO, and also for an external device. Please refer to the Appendix I0_MUX of this datasheet for more details.
² When VDD_SDIO operates at 3.3 V, it is driven directly by VDD3P3_RTC through a 6 Ω resistor, therefore there will be some voltage drop from VDD3P3_RTC.

³ The operating temperature of ESP32-U4WDH and ESP32-D0WDRH2-V3 ranges from -40 °C to 85 °C due to the in-package flash or PSRAM. For other chips that have no in-package flash or PSRAM, their operating temperature is approximately -40 °C ~ 125 °C.

---

**Additional Information:**
- VDD_SDIO can also be driven by an external power supply.
- Please refer to Section 2.5.2 Power Scheme for more information on the minimum voltage requirements and comparisons with other chips that have no in-package flash or PSRAM, their operating temperature is approximately -40 °C ~ 125 °C.

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32 Series Datasheet v5.2