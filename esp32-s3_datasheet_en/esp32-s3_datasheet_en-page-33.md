Title: Boot Configurations

Body Text:
The timing of signals connected to the strapping pins should adhere to the setup time and hold time specifications in Table 3-2 and Figure 3-1.

Table Title: Table 3-2. Description of Timing Parameters for the Strapping Pins

| Parameter | Description | Min (ms) |
|-----------|-------------|----------|
| t<sub>SU</sub> | Setup time is the time reserved for the power rails to stabilize before the CHIP_PU pin is pulled high to activate the chip. | 0 |
| t<sub>H</sub> | Hold time is the time reserved for the chip to read the strapping pin values after CHIP_PU is already high and before these pins start operating as regular IO pins. | 3 |

Figure Caption: Figure 3-1. Visualization of Timing Parameters for the Strapping Pins

Subtitle: 3.1 Chip Boot Mode Control

Body Text:
GPIO0 and GPIO46 control the boot mode after the reset is released. See Table 3-3 Chip Boot Mode Control.

Table Title: Table 3-3. Chip Boot Mode Control

| Boot Mode | GPIO0 | GPIO46 |
|-----------|-------|--------|
| SPI boot mode | 1 | Any value |
| Joint download boot mode | 0 | 0 |

Note:
1 Bold marks the default value and configuration.
2 Joint Download Boot mode supports the following
   - USB Download Boot: 
     - USB-Serial-JTAG Download Boot
     - USB-OTG Download Boot
   - UART Download Boot

Additional Information:
In addition to SPI Boot and Joint Download Boot modes, ESP32-S3 also support SPI Download Boot mode.

Footer Text (Company Name): Espressif Systems

Page Number: 33

Link Texts/Buttons:
- Submit Documentation Feedback