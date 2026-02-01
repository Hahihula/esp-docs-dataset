Title: Appendix A – ESP32-C5 Consolidated Pin Overview

Subtitle: Table 7-1. Pin Overview

Table:
| Pin No. | Pin Name | Type | Pin Providing Power At Reset | Pin Settings After Reset (0/1) | Analog Function | LP IO MUX Function |
|---------|----------|------|--------------------------------|----------------------------------|-----------------|--------------------|
|         |          |      |                               |                                   |                 |                    |
| 1       | VDDA6   | Power |                               |                                   |                 |                    |
| 2       | GND     | Power |                               |                                   |                 |                    |
| 3       | VDDA7   | Power |                               |                                   |                 |                    |
| 4       | XTAL_N  | Analog |                              |                                   |                 |                    |
| 5       | XTAL_P  | Analog |                              |                                   |                 |                    |
| 6       | VDDA8   | Power |                               |                                   |                 |                    |
| 7       | CHIP PU | Analog | VDDPST1                        |                                   |                 |                    |
| 8       | VDDP1   | Power |                               |                                   |                 |                    |
| 9       | XTAL_32K_P | VDDPST1 |                              | XTAL_32K_P                       | LP_GPI00        | I/O/OT              |
| 10      | XTAL_32K_N | VDDPST1 |                              | XTAL_32K_N                       | ADC1_CH0        | I/O/OT              |
| 11      | MTMS    | IO    | VDDPST1                        |                                   | LP_GPI02        | FSPIO              |
| 12      | MTDI    | IO    | VDDPST1                        |                                   | LP_GPI03        | I/O/OT              |
| 13      | MTCK    | IO    | VDDPST1                        |                                   | LP_GPI04        | FSPIO              |
| 14      | MTDIO   | IO    | VDDPST1                        |                                   | LP_GPI05        | I/O/OT              |
| 15      | GPIO6   | IO    | VDDPST1                        |                                   | LP_GPI06        | FSPIO              |
| 16      | GPIO7   | IO    | VDDPST1                        |                                   | LP_GPI07        | I/O/OT              |
| 17      | GPIO8   | IO    | VDDPST1                        |                                   | LP_GPI08        | FSPIO              |
| 18      | GPIO9   | IO    | VDDPST1                        |                                   | LP_GPI09        | I/O/OT              |
| 19      | GPIO10  | IO    | VDDPST1                        |                                   | LP_GPI10        | FSPIO              |
| 20      | UOTXD   | IO    | VDDPST1                        |                                   | LP_GPI11        | I/O/OT              |
| 21      | UORXD   | IO    | VDDPST1                        |                                   | LP_GPI12        | FSPIO              |
| 22      | GPIO13  | IO    | VDDPST2                        |                                   | LP_GPI13        | I/O/OT              |
| 23      | GPIO14  | IO    | VDDPST2                        |                                   | LP_GPI14        | FSPIO              |
| 24      | VPPower2 | Power |                               |                                   |                 |                    |
| 25      | SPICSI   | WPU   | VDD_SPI                         |                                   | SPICSI          | I/O/OT              |
| 26      | SPICS0   | IO    | VDD_SPI                         |                                   | SPICS0          | I/O/OT              |
| 27      | SPIQ     | IO    | WPU                             |                                   | SPIQ            | I/O/OT              |
| 28      | SPIWP    | IO    | WPU                             |                                   | SPIWP           | I/O/OT              |
| 29      | VDD_SPI  | Power/IO |                              |                                   |                 |                    |
| 30      | SPIHD   | IO    | VDD_SPI                         |                                   | SPIHD           | I/O/OT              |
| 31      | SPICLK  | IO    | WPU                             |                                   | SPICLK          | I/O/OT              |
| 32      | SPID     | IO    | WPU                             |                                   | SPID            | I/O/OT              |
| 33      | GPIO23  | VDDPST3                        |                                   | LP_GPI04        | FSPIO              |
| 34      | GPIO24  | VDDPST3                        |                                   | LP_GPI05        | FSPIO              |
| 35      | GPIO25  | IO    | VDDPST3                        |                                   | LP_GPI06        | FSPIO              |
| 36      | GPIO26  | IO    | VDDPST3                        |                                   | LP_GPI07        | FSPIO              |
| 37      | GPIO27  | IO    | IE, WPU                         |                                   | LP_GPI08        | FSPIO              |
| 38      | GPIO28  | IE, WPU                         |                                   | LP_GPI09        | FSPIO              |
| 39      | VDDP3   | Power |                               |                                   |                 |                    |
| 40      | VDDA1   | Power |                               |                                   |                 |                    |

(Note: The table continues on the next page, as indicated by "Cont'd on next page".)