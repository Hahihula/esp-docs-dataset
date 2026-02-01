**Title:**
3 Pin Definitions

**Table Title:**
Table 3-1. Pin Definitions

| Name | No.       | Type^1 | Function                                    |
|------|-----------|--------|----------------------------------------------|
| GND  | 1, 2, 11, 14, 36-53 | P     | Ground                                      |
|      |           |        |                                              |
| 3V3  | 3         | P     | Power supply                                |
|      |           |        |                                              |
| NC   | 4, 7, 9, 10, 15, 17, 24, 25, 28, 29, 32-35 | —    | NC                                           |
|      |           |        |                                              |
| IO2  | 5         | I/O/† | GPIO2, ADC1_CH2, FSPIQ                      |
| IO3  | 6         | I/O/† | GPIO3, ADC1_CH3                             |
| EN   | 8         | I     | High: on, enables the chip.                 |
|      |           |        | Low: off, the chip powers off.              |
|      |           |        | Note: Do not leave the EN pin floating       |
| IO0  | 12        | I/O/† | GPIO0, ADC1_CHO, XTAL_32K_P                 |
| IO1  | 13        | I/O/† | GPIO1, ADC1_CH1, XTAL_32K_N                |
| IO10 | 16        | I/O/† | GPIO10, FSPICSO                            |
| IO4  | 18        | I/O/† | GPIO4, ADC1_CH4, FSPIHD, MTMS              |
| IO5  | 19        | I/O/† | GPIO5, ADC2_CHO, FSPIWP, MTDI              |
| IO6  | 20        | I/O/† | GPIO6, FSPICLK, MTCK                        |
| IO7  | 21        | I/O/† | GPIO7, FSPID, MTDO                          |
| IO8  | 22        | I/O/† | GPIO8                                       |
| IO9  | 23        | I/O/† | GPIO9                                       |
| IO18 | 26        | I/O/† | GPIO18, USB_D-                              |
| IO19 | 27        | I/O/† | GPIO19, USB_D+                              |
| RXD0 | 30        | I/O/† | GPIO20, UORXD                               |
| TXD0 | 31        | I/O/† | GPIO21, UOTXD                               |

**Footnote:**
^1 P: power supply; I: input; O: output; T: high impedance.

**Footer Information:**
Espressif Systems
Page number: 11

Submit Documentation Feedback  
ESP32-C3-MINI-1 & MINI-1U Datasheet v2.1