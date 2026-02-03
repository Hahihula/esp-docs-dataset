**Title: Table 2-3. Power Pins**

| Pin No. | Pin Name       | Direction    | Power Domain / Other | IO Pins |
|---------|---------------|--------------|----------------------|---------|
| 1       | VDDA          | Input        | Analog power domain  |         |
| 3       | VDD3P3        | Input        | Analog power domain  |         |
| 4       | VDD3P3        | Input        | Analog power domain  |         |
| 19      | VDD3P3_RTC^1 | Input        | RTC and part of Digital power domains | RTC IO |
| 26      | VDD3P3_SDIO^2| Input/Output | Analog power domain  |         |
| 37      | VDD3P3_CPU^3 | Input        | Digital power domain | Digital IO |
| 43      | VDDA          | Input        | Analog power domain  |         |
| 46      | VDDA          | Input        | Analog power domain  |         |
| 49      | GND           | -            | External ground connection |       |

**Footnotes:**
1. VDD3P3_RTC is also the input power supply for RTC and CPU.
2. VDD_SDIO connects to the output of an internal LDO whose input is VDD3P3_RTC. When VDD_SDIO is connected to the same PCB net together with VDD3P3_RTC, the internal LDO is disabled automatically.
3. VDD3P3_CPU is also the input power supply for CPU.

**Subtitle: 2.5.2 Power Scheme**

The text mentions that "The power scheme is shown in Figure 2-3 ESP32 Power Scheme."

**Figure Caption:** 
"Figure 2-3. ESP32 Power Scheme"

**Diagram Description (from left to right, top to bottom):**
- VDD3P3_RTC connected with a line labeled "1.8V"
- LDO
- R = 6Ω resistor symbol leading down from the previous component and connecting back up.
- Another connection leads out of this point towards another label indicating "3.3V/1.8V" which is then split into two paths:
  - One path goes to VDD_SDIO labeled as part of SDIO Domain
  - The other continues through a line leading down from the previous component and connects back up, splitting again with one branch going towards another label indicating "1.1V", connected via LDO.
- Two more connections lead out:
  - One path goes to VDD3P3_CPU labeled as part of CPU Domain
  - The other continues through a line leading down from the previous component and connects back up, splitting again with one branch going towards another label indicating "1.1V", connected via LDO.

**Footer:**
- Espressif Systems
- ESP32 Series Datasheet v5.2

**Link:** 
"Submit Documentation Feedback"

(Note: The superscript numbers (1^ to 3^) refer back to the footnotes provided in Table 2-3.)