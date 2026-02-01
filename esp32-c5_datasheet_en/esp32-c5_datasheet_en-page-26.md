**Title:**
2 Pins

**Figure Caption (Top):**
Figure 2-2. ESP32-C5 Power Scheme.

**Body Text and Subtitle:**
2.5.3 Chip Power-up and Reset

Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_PU – the pin used for power-up and reset - should be pulled high to activate the chip. For information on CHIP_PU as well as power-up and reset timing, see Figure 2-3 and Table 2-11.

**Figure Caption (Bottom):**
Figure 2-3. Visualization of Timing Parameters for Power-up and Reset

**Diagram Labels:**
VDDPST1
VDDPST2
VDDPST3
VDDAX
LP Voltage Regulator
HP Voltage Regulator
Analog
RSPI
VDD_SPI
LP IO
LP System
HP System
HP IO0, HP IO1
Flash IO

**Diagram Labels (Additional):**
CHIP_PU
VIL_NRHST

**Footer:**
Espressif Systems  
26  
Submit Documentation Feedback  

**Series Datasheet Information:**  
ESP32-C5 Series Datasheet v1.0