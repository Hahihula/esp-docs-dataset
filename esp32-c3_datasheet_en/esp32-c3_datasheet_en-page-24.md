Title: Table 2-7. Peripheral Pin Assignment

| Pin No. | Pin Name       | USB Serial/JTAG | JTAG   | ADC1    | ADC2     | UARTO^2 | SPI0/1^2 | SPI1^2 | I2C      | I2S      | TWAI     | LED PWM  | RMT        |
|---------|---------------|-----------------|--------|---------|----------|---------|----------|--------|----------|----------|----------|-----------|
| 1       | LNA_IN        |                  |        |         |          |         |          |        |          |         |          |           |
| 2       | VDD3P3        |                  |        |         |          |         |          |        |          |         |          |           |
| 3       | VDD3P3        |                  |        |         |          |         |          |        |          |         |          |           |
| 4       | XTAL_32K_P    |                  |        |         |          |         |          |        |          |         |          |           |
| 5       | XTAL_32K_N   |                 |        |         |          |         |          |        |          |         |          |           |
| 6       | GPIO2         |                  |        |         |          |         |          |        |          |         |          |           |
| 7       | CHIP_EN       |                  |        |         |          |         |          |        |          |         |          |           |
| 8       | GPIO3         |                  |        |         |          |         |          |        |          |         |          |           |
| 9       | MTMS          |                  |        |         |          |         |          |        |          |         |          |           |
| 10      | MTDI          |                  |        |         |          |         |          |        |          |         |          |           |
| 11      | VDD3P3_RTC    |                  |        |         |          |         |          |        |          |         |          |           |
| 12      | MTCK          |                  |        |         |          |         |          |        |          |         |          |           |
| 13      | MTD0          |                  |        |         |          |         |          |        |          |         |          |           |
| 14      | GPIO8         |                  |        |         |          |         |          |        |          |         |          |           |
| 15      | GPIO9         |                  |        |         |          |         |          |        |          |         |          |           |
| 16      | GPIO10        |                  |        |         |          |         |          |        |          |         |          |           |
| 17      | VDD3P3_CPU    |                  |        |         |          |         |          |        |          |         |          |           |
| 18      | VDD_SPI       |                  |        |         |          |         |          |        |          |         |          |           |
| 19      | SPIHD         |                  |        |         |          |         |          |        |          |         |          |           |
| 20      | SPIWP         |                  |        |         |          |         |          |        |          |         |          |           |
| 21      | SPICSO        |                  |        |         |          |         |          |        |          |         |          |           |
| 22      | SPICLK        |                  |        |         |          |         |          |        |          |         |          |           |
| 23      | SPIQ          |                  |        |         |          |         |          |        |          |         |          |           |
| 24      | SPID          |                  |        |         |          |         |          |        |          |         |          |           |
| 25      | GPIO18        | USB_D- (PI)    |        |         |          |         |          |        |          |         |          |           |
| 26      | GPIO19        | USB_D+ (PI)    |        |         |          |         |          |        |          |         |          |           |
| 27      | UORXD         |                  |        |         |          |         |          |        |          |         |          |           |
| 28      | UOTXD         |                  |        |         |          |         |          |        |          |         |          |           |
| 29      | XTAL_N        |                  |        |         |          |         |          |        |          |         |          |           |
| 30      | XTAL_P        |                  |        |         |          |         |          |        |          |         |          |           |
| 31      | VDDA          |                  |        |         |          |         |          |        |          |         |          |           |
| 32      | VDD            |                  |        |         |          |         |          |        |          |         |          |           |
| 33      | GND           |                  |        |         |          |         |          |        |          |         |          |           |

Footnotes:
1 For USB Serial/JTAG, the USB_D- and USB_D+ can be swapped by configuring the USB_SERIAL_JTAG_EXCHG_PINS bit according to [ESP32-C3 Technical Reference Manual](#).
2 Signals of UARTO, SPI0/1, and SPI2 interface can be mapped to any GPIO pins through the GPIO Matrix, regardless of whether they are directly routed via fixed pins or IO MUX.

Note: The image contains a table with multiple columns representing different pin assignments for various peripherals. Each row corresponds to an individual pin number (from 1 to 33) and lists which functions can be assigned to that pin based on the specified headers such as USB Serial/JTAG, JTAG, ADC1, etc.

The bottom of the image contains two footnotes explaining how certain configurations work for specific pins related to USB Serial/JTAG. The references are indicated by superscript numbers (e.g., ^2) which correspond to explanations provided in a separate section below or within parentheses next to some entries like "ESP32-C3 Technical Reference Manual".