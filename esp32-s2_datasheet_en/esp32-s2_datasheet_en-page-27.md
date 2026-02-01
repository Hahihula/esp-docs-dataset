**Title:**
2 Pins

**Figure Caption (Top):**
Figure 2-2. ESP32-S2 Power Scheme

**Subsection Title and Description:**
2.5.3 Chip Power-up and Reset

**Body Text:**
Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_PU – the pin used for power-up and reset – is pulled high to activate the chip. For information on CHIP_PU as well as power-up and reset timing, see Figure 2-3 and Table 2-13.

**Table Title:**
Table 2-13. Description of Timing Parameters for Power-up and Reset

| Parameter | Description |
|-----------|-------------|
| t_STBL    | Time reserved for the power rails of VDDA, VDD3P3, VDD3P3_RTC, VDD3P3_RTC_IO, and VDD3P3_CPU to stabilize before the CHIP_PU pin is pulled high to activate the chip |
| t_RST     | Time reserved for CHIP_PU to stay below V_IL_nRST to reset the chip (see Table 5-4) |

**Figure Caption:**
Figure 2-3. Visualization of Timing Parameters for Power-up and Reset

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-S2 Series Datasheet v1.8  

**Page Number:** 
27