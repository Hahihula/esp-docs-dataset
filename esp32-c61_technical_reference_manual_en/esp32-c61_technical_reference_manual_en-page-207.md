
```markdown
| Target                                       | Boundary Address Low Address | High Address   | Size (KB) |
|----------------------------------------------|------------------------------|----------------|-----------|
| Reserved                                     | 0x6009_4000                  | 0x6009_4FFF    |           |
| HP System Registers (HP_SYSREG)              | 0x6009_5000                  | 0x6009_5FFF    | 4         |
| Power/Clock/Reset Registers (PCR)            | 0x6009_6000                  | 0x6009_6FFF    | 4         |
| Reserved                                     | 0x6009_7000                  | 0x6009_7FFF    |           |
| Trusted Execution Environment (TEE)²         | 0x6009_8000                  | 0x6009_8FFF    | 4         |
| High-Performance Access Permission Management (HP_APM) | 0x6009_9000                  | 0x6009_9FFF    | 4         |
| CPU Access Permission Management (CPU_APM)   | 0x6009_A000                  | 0x6009_AFFF    | 4         |
| Reserved                                     | 0x6009_B000                  | 0x600A_FFFF    |           |
| Power Management Unit (PMU)                  | 0x600B_0000                  | 0x600B_03FF    | 1         |
| Low-Power Clock/Reset Registers (LP_CLKRST) | 0x600B_0400                  | 0x600B_07FF    | 1         |
| Reserved                                     | 0x600B_0800                  | 0x600B_0BFF    |           |
| Low-Power Timer (LP_TIMER)                   | 0x600B_0C00                  | 0x600B_0FFF    | 1         |
| Low-Power Always-on Registers (LP_AON)       | 0x600B_1000                  | 0x600B_13FF    | 1         |
| Reserved                                     | 0x600B_1400                  | 0x600B_1BFF    |           |
| Low-Power Watchdog Timer (LP_WDT)            | 0x600B_1C00                  | 0x600B_1FFF    | 1         |
| Reserved                                     | 0x600B_2000                  | 0x600B_23FF    |           |
| Low-Power Peripherals (LPPERI)               | 0x600B_2800                  | 0x600B_2BFF    | 1         |
| Low-Power Analog Peripherals (LP_ANA_PERI)   | 0x600B_2C00                  | 0x600B_2FFF    | 1         |
| Reserved                                     | 0x600B_3000                  | 0x600B_37FF    |           |
| Low-Power Access Permission Management (LP_APM)² | 0x600B_3800                  | 0x600B_3BFF    | 1         |
| Reserved                                     | 0x600B_3C00                  | 0x600B_3FFF    |           |
| Low-Power IO MUX (LP_IO_MUX)                 | 0x600B_4000                  | 0x600B_43FF    | 1         |
| Low-Power GPIO Matrix (LP_GPIO)              | 0x600B_4400                  | 0x600B_47FF    | 1         |
| eFuse Controller                              | 0x600B_4800                  | 0x600B_4FFF    | 2         |
| Reserved                                     | 0x600B_5000                  | 0x600B_FFFF    |           |
| RISC-V Trace Encoder (TRACE)                 | 0x600C_0000                  | 0x600C_0FFF    | 4         |
| Reserved                                     | 0x600C_1000                  | 0x600C_1FFF    |           |
| Bus Access Monitor (BUS_MONITOR)²            | 0x600C_2000                  | 0x600C_2FFF    | 4         |
| Reserved                                     | 0x600C_3000                  | 0x600C_4FFF    |           |
| Interrupt Priority Registers (INTPRI)        | 0x600C_5000                  | 0x600C_5FFF    | 4         |
| Reserved                                     | 0x600C_6000                  | 0x600C_7FFF    |           |
| Cache                                        | 0x600C_8000                  | 0x600C_8FFF    | 4         |
| Reserved                                     | 0x600C_9000                  | 0x600C_FFFF    |           |

```