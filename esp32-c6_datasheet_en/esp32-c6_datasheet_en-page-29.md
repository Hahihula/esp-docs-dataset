**Title:**
2 Pins

**Subtitle:**
2.5 Power Supply

**Subsection Title:**
2.5.1 Power Pins

**Body Text:**
The chip is powered via the power pins described in Table 2-13 Power Pins.

**Table Header (Table 2-13):**
- QFN40
- Pin No.
- Name
- Direction
- Power Domain / Other
- IO Pins

**Table Content:**
| Pin | Pin No. | Name       | Direction | Power Domain / Other                   | IO Pins |
|-----|---------|------------|-----------|----------------------------------------|---------|
| 2   | VDDA3P3 | Input      | Analog power domain                      |         |
| 3   | VDDA3P3 | Input      | Analog power domain                      |         |
| 5   | VDDPST1 | Input      | LP digital and part of analog pin power domains | LP IO^3|
| 23  | VDD_SPI | Input      | In-package flash (backup power line)     |         |
| 28  | VDDPST2 | Input      | HR digital power domain                   | HP IO^1|
| 37  | VDDA1   | Input      | Analog power domain                      |         |
| 40  | VDDA2   | Input      | Analog power domain                      |         |
| 41  | GND     | —          | External ground connection               |         |

**Footnotes:**
1. See in conjunction with Section 2.5.2 Power Scheme.
2. For recommended and maximum voltage and current, see Section 5.1 Absolute Maximum Ratings and Section 5.2 Recommended Operating Conditions.

3. LP IO pins are those powered by VDDPST1 and so on, as shown in Figure 2-3 ESP32-C6 Power Scheme.

**Additional References:**
See also Table 2-1 QFN40 Pin Overview or Table 2-2 QFN32 Pin Overview > Column Pin Providing Power.

**Subsection Title:**
2.5.2 Power Scheme

**Body Text:**
The power scheme is shown in Figure 2-3 ESP32-C6 Power Scheme.
The components on the chip are powered via voltage regulators.

**Table Header (Table 2-14):**
- Voltage Regulator
- Output
- Power Supply

**Table Content:**
| Voltage Regulator | Output   | Power Supply |
|-------------------|----------|-------------|
| HP                | HR       | HP power domain |
| LP                | LP power domain |

**Footer Text:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-C6 Series Datasheet v1.4

**Page Number:** 29