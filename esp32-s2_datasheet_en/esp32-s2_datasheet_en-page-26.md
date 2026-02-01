**Title:**
2 Pins

**Subtitle:**
2.5 Power Supply

**Subsection Title:**
2.5.1 Power Pins

**Body Text:**
The chip is powered via the power pins described in Table 2-11 Power Pins.

**Table Header (Table 2-11):**
Pin No., Pin Name, Direction, Power Domain/Other, IO Pins

| Pin No. | Pin Name       | Direction | Power Domain/Other                   | IO Pins                  |
|---------|---------------|-----------|--------------------------------------|--------------------------|
| 1       | VDDA          | Input     | Analog power domain                   |                         |
| 3       | VDD3P3        | Input     | Analog power domain                   |                         |
| 4       | VDD3P3        | Input     | Analog power domain                   |                         |
| 20      | VDD3P3_RTC    | Input     | RTC domain                            |                         |
| 27      | VDD3P3_RTC_IO | Input     | RTC and part of Digital power domains | RTC IO                  |
| 30      | VDD_SPI_3.4   | Input     | In-package memory (backup power line) |                         |
| 45      | VDD3P3_CPU    | Input     | Digital power domain                  | Digital IO               |
| 51      | VDDA          | Input     | Analog power domain                   |                         |
| 54      | VDDA          | Input     | Analog power domain                   |                         |
| 57      | GND           | —         | External ground connection            |                         |

**Footnotes:**
1. See in conjunction with Section 2.5.2 Power Scheme.
2. For recommended and maximum voltage and current, see Section 5.1 Absolute Maximum Ratings and Section 5.2 Recommended Operating Conditions.

3. To configure VDD_SPI as input or output, see ESP32-S2 Technical Reference Manual > Chapter Low-power Management.

4. To configure output voltage, see Section 3.2 VDD_SPI Voltage Control and Section 5.3 VDD_SPI Output Characteristics.
5. RTC IO pins are those powered by VDD3P3_RTC_IO and so on...

**Additional Information:**
ESP32-S2 Power Scheme. See also Table 2-1 Pin Overview > Column Pin Providing Power.

**Subsection Title:**
2.5.2 Power Scheme

**Body Text:**
The power scheme is shown in Figure 2-2 ESP32-S2 Power Scheme.
The components on the chip are powered via voltage regulators.

**Table Header (Table 2-12):**
Voltage Regulator, Output Voltage, Power Supply

| Digital | Low-power | Flash |
|---------|-----------|-------|
| 1.1 V   | 1.1 V     | 1.8 V |

**Body Text:**
Digital power domain
RTC power domain
Can be configured to power in-package flash/PSRAM or off-package memory

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
26  
ESP32-S2 Series Datasheet v1.8