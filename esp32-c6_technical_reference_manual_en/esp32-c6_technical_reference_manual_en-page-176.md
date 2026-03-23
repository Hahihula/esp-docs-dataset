

```markdown
| Target                                       | Boundary Address          | Size (KB) |
|----------------------------------------------|----------------------------|-----------|
| HMAC Accelerator (HMAC)                      | Low Address               | High Address |           |
|                                              | 0x6008_D000                | 0x6008_DFFF   | 4         |
| Reserved                                     | 0x6008_E000                | 0x6008_FFFF   |           |
| IO MUX                                       | 0x6009_0000                | 0x6009_0FFF   | 4         |
| GPIO Matrix                                  | 0x6009_1000                | 0x6009_1FFF   |           |
| Memory Access Monitor (MEM_MONITOR)*         | 0x6009_2000                | 0x6009_2FFF   | 4         |
| Reserved                                     | 0x6009_4000                | 0x6009_4FFF   |           |
| HP System Register (HP_SYSREG)               | 0x6009_5000                | 0x6009_5FFF   | 4         |
| Power/Clock/Reset (PCR) Register             | 0x6009_6000                | 0x6009_6FFF   |           |
| Reserved                                     | 0x6009_7000                | 0x6009_7FFF   |           |
| Trusted Execution Environment (TEE) Register*| 0x6009_8000                | 0x6009_8FFF   | 4         |
| Access Permission Management Controller      | 0x6009_9000                | 0x6009_9FFF   |           |
|(HP_APM)*                                     |||||
| Reserved                                     | 0x6009_A000                | 0x600A_FFFF   |           |
| Power Management Unit (PMU)                   | 0x600B_0000                | 0x600B_03FF   | 1         |
| Low-power Clock/Reset Register               | 0x600B_0400                | 0x600B_07FF   |           |
|(LP_CLKRST)                                  |||||
| eFuse Controller (EFUSE)                      | 0x600B_0800                | 0x600B_0BFF   | 1         |
| RTC Timer (RTC_TIMER)                         | 0x600B_0C00                | 0x600B_0FFF   |           |
| Low-power Always-on Register                 | 0x600B_1000                | 0x600B_13FF   | 1         |
| Low-power UART (LP_UART)                      | 0x600B_1400                | 0x600B_17FF   |           |
| Low-power I2C (LP_I2C)                        | 0x600B_1800                | 0x600B_1BFF   |           |
| RTC Watch Dog Timer (RTC_WDT)                 | 0x600B_1C00                | 0x600B_1FFF   |           |
| Low-power IO MUX (LP_IO MUX)                  | 0x600B_2000                | 0x600B_23FF   |           |
| I2C Analog Master (I2C_ANA_MST)               | 0x600B_2400                | 0x600B_27FF   |           |
| Low-power Peripheral (LP_PERI)                | 0x600B_2800                | 0x600B_2BFF   |           |
| Low-power Analog Peripheral (LP_ANA_PERI)     | 0x600B_2C00                | 0x600B_2FFF   |           |
| Reserved                                     | 0x600B_3000                | 0x600B_33FF   |           |
| Low-power Trusted Execution Environment       | 0x600B_3400                | 0x600B_37FF   |           |
|(LP_TEE)*                                     |||||
| Low-power Access Permission Management        | 0x600B_3800                | 0x600B_3BFF   |           |
|(LP_APM)*                                     |||||
| Reserved                                     | 0x600B_3C00                | 0x600B_FFFF   |           |
| RISC-V Trace Encoder (TRACE)                  | 0x600C_0000                | 0x600C_0FFF   | 4         |
| Reserved                                     | 0x600C_1000                | 0x600C_1FFF   |           |
| DEBUG ASSIST (ASSIST_DEBUG)*                  | 0x600C_2000                | 0x600C_2FFF   |           |
| Reserved                                     | 0x600C_3000                | 0x600C_4FFF   |           |
| Interrupt Priority Register (INTPRI)          | 0x600C_5000                | 0x600C_5FFF   |           |
| Reserved                                     | 0x600C_6000                | 0x600C_FFFF   |           |

\* The address space of this module/peripheral is not continuous.
```