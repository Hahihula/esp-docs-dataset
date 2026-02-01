**Title:**
2 Pins

**Figure Caption (Top):**
Figure 2-3. ESP32-C6 Power Scheme

**Subsection Title and Body Text:**
2.5.3 Chip Power-up and Reset

Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_PU – the pin used for power-up and reset – is pulled high to activate the chip. For information on CHIP_PU as well as power-up and reset timing, see Figure 2-4 and Table 2-15.

**Figure Caption (Bottom):**
Figure 2-4. Visualization of Timing Parameters for Power-up and Reset

**Table:**
| t_STBL | VDDA3P3, VDDPST1 |
|--------|------------------|
|        | VDDPST2, VDDAI1, VDDA2 |

**Footer Information:**
Espressif Systems
Submit Documentation Feedback ESP32-C6 Series Datasheet v1.4

**Page Number:** 30