Title: Boot Configurations

Body Text:
All strapping pins have latches. At Chip Reset, the latches sample the bit values of their respective strapping pins and store them until the chip is powered down or shut down. The states of latches cannot be changed in any other way. It makes the strapping pin values available during the entire chip operation, and the pins are freed up to be used as regular IO pins after reset. For details on Chip Reset, see ESP32-C5 Technical Reference Manual > Chapter Reset and Clock.

The timing of signals connected to the strapping pins should adhere to the setup time and hold time specifications in Table 4-2 and Figure 4-1.

Table Title: Table 4-2. Description of Timing Parameters for the Strapping Pins

| Parameter | Description |
|-----------|-------------|
| tSU       | Setup time is the time reserved for the power rails to stabilize before the CHIP_PU pin is pulled high to activate the chip. |
| tH        | Hold time is the time reserved for the chip to read the strapping pin values after CHIP_PU is already high and before these pins start operating as regular IO pins. |

Figure Caption: Figure 4-1. Visualization of Timing Parameters for the Strapping Pins

Subtitle:
4.1 Chip Boot Mode Control

Body Text (continued):
GPIO26, GPIO27 and GPIO28 control the boot mode after the reset is released. See Table 4-3 Boot Mode Control.

Footer Information: 
Espressif Systems
Page Number: 14
Document Title: ESP32-C5-MINI-1 Datasheet v1.0

Link Text:
Submit Documentation Feedback