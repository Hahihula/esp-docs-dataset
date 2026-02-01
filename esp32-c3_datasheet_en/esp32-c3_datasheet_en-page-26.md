**Title:**
2 Pins

**Subtitle:**
2.5 Power Supply

**Subsection Title:**
2.5.1 Power Pins

**Body Text:**
The chip is powered via the power pins described in Table 2-9 Power Pins.

**Table Header (Table 2-9):**
| Pin No. | Pin Name | Direction | Power Domain / Other | IO Pins |
|---------|----------|-----------|----------------------|--------|
| 2       | VDD3P3  | Input     | Analog power domain  |        |
| 3       | VDD3P3  | Input     | Analog power domain  |        |
| 11      | VDD3P3_RTC | Input    | RTC and part of Digital power domains | RTC IO |
| 17      | VDD3P3_CPU | Input    | Digital power domain | Digital IO |
| 18      | VDD_SPI4 | Input     | In-package flash (backup power line) |        |
|         |          | Output    | In-package and off-package flash | SPIIO |
| 31      | VDDA     | Input     | Analog power domain  |        |
| 32      | VDDA     | Input     | Analog power domain  |        |
| 33      | GND      | —         | External ground connection |        |

**Footnotes:**
1. See in conjunction with Section **2.5.2 Power Scheme**.
2. For recommended and maximum voltage and current, see Section *5.1 Absolute Maximum Ratings* and Section *5.2 Recommended Operating Conditions*.
3. Digital IO pins are those powered by VDD3P3_CPU, and RTC IO pins are those powered by VDD3P3_RTC and so on, as shown in Figure 2-3 ESP32-C3 Power Scheme.

**Additional Information:**
See also Table *2-1 Pin Overview* > Column Pin Providing Power.
To configure VDD_SPI as input or output, see *ESP32-C3 Technical Reference Manual* > Chapter Low-power Management.

**Subsection Title:**
2.5.2 Power Scheme

**Body Text:**
The power scheme is shown in Figure 2-3 ESP32-C3 Power Scheme.
The components on the chip are powered via voltage regulators.

**Table Header (Table 2-10):**
| Voltage Regulator | Output    | Power Supply |
|--------------------|-----------|--------------|
| Digital            |           | Digital power domain |
| Low-power          |           | RTC power domain |

**Footer:**
Espressif Systems
ESP32-C3 Series Datasheet v2.2

**Link Texts:**
- Submit Documentation Feedback