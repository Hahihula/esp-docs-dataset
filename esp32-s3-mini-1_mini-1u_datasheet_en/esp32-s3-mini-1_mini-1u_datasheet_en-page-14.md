Title: **4 Boot Configurations**

Body Text:
any other way. It makes the strapping pin values available during the entire chip operation, and the pins are freed up to be used as regular IO pins after reset.

The timing of signals connected to the strapping pins should adhere to the setup time and hold time specifications in Table 4-2 and Figure 4-1.

Table: **Table 4-2. Description of Timing Parameters for the Strapping Pins**

| Parameter | Description | Min (ms) |
|-----------|-------------|----------|
| t<sub>SU</sub> | Setup time is the time reserved for the power rails to stabilize before the EN pin is pulled high to activate the chip. | 0 |
| t<sub>H</sub> | Hold time is the time reserved for the chip to read the strapping pin values after EN is already high and before these pins start operating as regular IO pins. | 3 |

Image Caption: **Figure 4-1. Visualization of Timing Parameters for the Strapping Pins**

Subtitle:
**4.1 Chip Boot Mode Control**

Body Text:
GPIO0 and GPIO46 control the boot mode after the reset is released. See Table 4-3 Chip Boot Mode Control.

Table: **Table 4-3. Chip Boot Mode Control**

| Boot Mode | GPIO0 | GPIO46 |
|-----------|-------|--------|
| SPI Boot 1 | 1     | Any value |
| Joint Download Boot 2 | 0    | 0      |

Footnotes:
1 Bold marks the default value and configuration.
2 Joint Download Boot mode supports the following download methods:

- USB Download Boot:
  - USB-Serial-JTAG Download Boot
  - USB-OTG Download Boot

- UART Download Boot

Footer: Espressif Systems, ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6 Submit Documentation Feedback