Title: Boot Configurations

Body Text:
any other way. It makes the strapping pin values available during the entire chip operation, and the pins are freed up to be used as regular IO pins after reset. For details on Chip Reset, see ESP32-C6 Technical Reference Manual > Chapter Reset and Clock.

The timing of signals connected to the strapping pins should adhere to the setup time and hold time specifications in Table 4-2 and Figure 4-1.

Table Title: Table 4-2. Description of Timing Parameters for the Strapping Pins

| Parameter | Description | Min (ms) |
|-----------|-------------|----------|
| t_SU      | Setup time is the time reserved for the power rails to stabilize before the CHIP_PU pin is pulled high to activate the chip. | 0        |
| t_H       | Hold time is the time reserved for the chip to read the strapping pin values after CHIP_PU is already high and before these pins start operating as regular IO pins. | 3        |

Image Caption: Figure 4-1. Visualization of Timing Parameters for the Strapping Pins

Subtitle: 4.1 Chip Boot Mode Control

Body Text:
GPI08 and GPI09 control the boot mode after the reset is released. See Table 4-3 Chip Boot Mode Control.

Table Title: Table 4-3. Chip Boot Mode Control

| Boot Mode | GPIO08 | GPIO09 |
|-----------|--------|--------|
| SPI boot mode | Any value | 1      |
| Joint download boot mode | 2 | 0 |

Note:
1 Bold marks the default value and configuration.
2 Joint Download Boot mode supports the following download methods:

- USB-Serial-JTAG Download Boot
- UART Download Boot
- SDIO Download Boot

Footer: Espressif Systems ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4 Submit Documentation Feedback