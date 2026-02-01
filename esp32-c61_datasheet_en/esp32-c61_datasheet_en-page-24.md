**Title:**
2 Pins

**Figure Caption (Top):**
Figure 2-2. ESP32-C61 Power Scheme

**Subtitle and Body Text:**
2.5.3 Chip Power-up and Reset

Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_PU – the pin used for power-up and reset – is pulled high to activate the chip. For information on CHIP_PU as well as power-up and reset timing, see Figure 2-3 and Table 2-10.

**Figure Caption (Middle):**
Figure 2-3. Visualization of Timing Parameters for Power-up and Reset

**Table Title:**
Table 2-10. Description of Timing Parameters for Power-up and Reset

| Parameter | Description | Min (\(\mu\)s) |
|-----------|-------------|---------------|
| \(t_{STBL}\) | Time reserved for the power rails of VDDA3, VDDA4, VDDPST1, VDDPST2, VDDA1 and VDDA2 to stabilize before the CHIP_PU pin is pulled high to activate the chip | 50 |
| \(t_{RST}\) | Time reserved for CHIP_PU to stay below \(V_{IL_n}^{RST}\) to reset the chip | 50 |

**Footer:**
Espressif Systems  
24 ESP32-C61 Series Datasheet v0.5