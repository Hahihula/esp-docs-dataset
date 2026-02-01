**Title:**
3 Boot Configurations

**Body Text:**
The timing of signals connected to the strapping pins should adhere to the setup time and hold time specifications in Table 3-2 and Figure 3-1.

**Table Title:**
Table 3-2. Description of Timing Parameters for the Strapping Pins

| Parameter | Description | Min (ms) |
|-----------|-------------|----------|
| t<sub>SU</sub> | Setup time is the time reserved for the power rails to stabilize before the CHIP_PU pin is pulled high to activate the chip. | 0 |
| t<sub>H</sub> | Hold time is the time reserved for the chip to read the strapping pin values after CHIP_PU is already high and before these pins start operating as regular IO pins. | 3 |

**Figure Caption:**
Figure 3-1. Visualization of Timing Parameters for the Strapping Pins

**Subsection Title:**
3.1 Chip Boot Mode Control

**Subsection Body Text:**
GPIO26, GPIO27 and GPIO28 control the boot mode after the reset is released. See Table 3-3 Boot Mode Control.

**Footer Information:**
Espressif Systems  
ESP32-C5 Series Datasheet v1.0  

**Link:**
Submit Documentation Feedback