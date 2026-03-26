

```markdown
| Target                                       | Boundary Address Low Address | High Address   | Size (KB) |
|----------------------------------------------|------------------------------|----------------|-----------|
| General Purpose SPI2 (GP-SPI2)               | 0x500D_0000                  | 0x500D_OFFF    | 4         |
| General Purpose SPI3 (GP-SPI3)               | 0x500D_1000                  | 0x500D_1FFF    | 4         |
| USB Serial/JTAG Controller                   | 0x500D_2000                  | 0x500D_2FFF    | 4         |
| LED PWM Controller (LEDC)                    | 0x500D_3000                  | 0x500D_3FFF    | 4         |
| Reserved                                     | 0x500D_4000                  | 0x500D_4FFF    |           |
| Event Task Matrix (SOC_ETM)                  | 0x500D_5000                  | 0x500D_5FFF    | 4         |
| Interrupt Matrix (INTMTX)                    | 0x500D_6000                  | 0x500D_6FFF    | 4         |
| Two-wire Automotive Interface 0 (TWAI0)      | 0x500D_7000                  | 0x500D_7FFF    | 4         |
| Two-wire Automotive Interface 1 (TWAI1)      | 0x500D_8000                  | 0x500D_8FFF    | 4         |
| Two-wire Automotive Interface 2 (TWAI2)      | 0x500D_9000                  | 0x500D_9FFF    | 4         |
| I3C Master Controller                        | 0x500D_A000                  | 0x500D_AFFF    | 4         |
| I3C Slave Controller                         |                              | 0x500D_BFFF    | 4         |
| LCD and Camera Controller (LCD_CAM)          | 0x500D_C000                  | 0x500D_CFFF    | 4         |
| Reserved                                     | 0x500D_D000                  | 0x500D_DFFF    |           |
| ADC Controller                               | 0x500D_E000                  | 0x500D_EFFF    | 4         |
| UHCI Controller (UHCI)                       | 0x500D_F000                  | 0x500D_FFFF    | 4         |
| GPIO Matrix                                  | 0x500E_0000                  | 0x500E_0FFF    | 4         |
| IO MUX                                       | 0x500E_1000                  | 0x500E_1FFF    | 4         |
| System Timer (SYSTIMER)                      | 0x500E_2000                  | 0x500E_2FFF    | 4         |
| Reserved                                     | 0x500E_3000                  | 0x500E_4FFF    |           |
| HP System Register (SYSREG)                  | 0x500E_5000                  | 0x500D_5FFF    | 4         |
| Reset and Clock                              | 0x500E_6000                  | 0x500E_6FFF    | 4         |
| Reserved                                     | 0x500E_7000                  | 0x500F_FFFF    |           |
| MIPI Camera and LCD Memory                   |                              |               |           |
| MIPI Camera Memory                           | 0x5010_4000                  | 0x5010_4FFF    | 4         |
| MIPI LCD Memory                              | 0x5010_5000                  | 0x5010_5FFF    | 4         |
| LP Always On Peripherals (LP AON PERI)       |                              |               |           |
| LP System Register                           | 0x5011_0000                  | 0x5011_0FFF    | 4         |
| LP Always-on Clock and Reset                 | 0x5011_1000                  | 0x5011_1FFF    | 4         |
| LP Timer                                     | 0x5011_2000                  | 0x5011_2FFF    | 4         |
| LP Analog peripherals (LP ANAPERI)           | 0x5011_3000                  | 0x5011_3FFF    | 4         |
| LP HUK                                       | 0x5011_4000                  | 0x5011_4FFF    | 4         |
| Power Management Unit (PMU)                  | 0x5011_5000                  | 0x5011_5FFF    | 4         |
| LP Watch Dog Timer (LP WDT)                  | 0x5011_6000                  | 0x5011_6FFF    | 4         |
| Reserved                                     | 0x5011_7000                  | 0x5011_7FFF    |           |
| LP Mailbox (LP MB)                           | 0x5011_8000                  | 0x5011_8FFF    | 4         |
| Reserved                                     | 0x5011_A000                  | 0x5011_FFFF    |           |
| LP Peripherals (LP PERI)                     |                              |               |           |
| LP Peripheral Clock and Reset (LP PERI-CLKRST)| 0x5012_0000                  | 0x5012_0FFF    | 4         |
| LP UART                                      | 0x5012_1000                  | 0x5012_1FFF    | 4         |

```