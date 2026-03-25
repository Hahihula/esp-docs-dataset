

```markdown
| Target | Boundary Address Low Address | High Address | Size (KB) |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------|:--------------|:-----------|
| Low-power Clock/Reset Register (LP_CLKRST) | 0x600B_0400 | 0x600B_07FF | 1 |
| eFuse Controller (EFUSE) | 0x600B_0800 | 0x600B_0BFF | 1 |
| Low-power Timer (LP_TIMER) | 0x600B_0C00 | 0x600B_0FFF | 1 |
| Low-power Always-on Register (LP_AON) | 0x600B_1000 | 0x600B_13FF | 1 |
| Reserved | 0x600B_1400 | 0x600B_1BFF |   |
| Low-power Watch Dog Timer (LP_WDT) | 0x600B_1C00 | 0x600B_1FFF | 1 |
| Reserved | 0x600B_2000 | 0x600B_27FF |   |
| Low-power Peripheral (LPPERI) | 0x600B_2800 | 0x600B_2BFF | 1 |
| Low-power Analog Peripheral (LP_ANA_PERI) | 0x600B_2C00 | 0x600B_2FFF | 1 |
| Reserved | 0x600B_3000 | 0x600B_37FF |   |
| Low-power Access Permission Management (LP_APM)* | 0x600B_3800 | 0x600B_3BFF | 1 |
| Reserved | 0x600B_3C00 | 0x600B_FFFF |   |
| RISC-V Trace Encoder (TRACE) | 0x600C_0000 | 0x600C_0FFF | 4 |
| Reserved | 0x600C_1000 | 0x600C_1FFF |   |
| DEBUG ASSIST (ASSIST_DEBUG)* | 0x600C_2000 | 0x600C_2FFF | 4 |
| Reserved | 0x600C_3000 | 0x600C_4FFF |   |
| Interrupt Priority Register (INTPRI) | 0x600C_5000 | 0x600C_5FFF | 4 |
| Reserved | 0x600C_6000 | 0x600C_FFFF |   |

* The address space of this module/peripheral is not continuous.
```