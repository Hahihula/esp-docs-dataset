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

**Body Text:**
GPIO8 and GPIO9 control the boot mode after the reset is released. See Table 3-3 Chip Boot Mode Control.

**Table Title:**
Table 3-3. Chip Boot Mode Control

| Boot Mode | GPIO8 | GPIO9 |
|-----------|-------|-------|
| SP boot mode | Any value | 1 |
| Joint download boot mode | 1 | 0 |

**Note in Table:**
1 Bold marks the default value and configuration.
2 Joint Download Boot mode supports the following download methods:
   - USB-Serial-JTAG Download Boot
   - UART Download Boot
   - SDIO Download Boot

**Footer Text:**
Espressif Systems  
34  
Submit Documentation Feedback