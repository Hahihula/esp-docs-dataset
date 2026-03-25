

```markdown
Chapter 7 Reset and Clock

Register 7.68. LP_CLKRST_CPU_RESET_REG (0x0014)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | LP_CLKRST_CPU_STALL_EN                                                     |
| 30  | LP_CLKRST_CPU_STALL_WAIT                                                  |
| 26  | LP_CLKRST_CPU_WDT_RESET_EN                                                |
| 25  | LP_CLKRST_RTC_WDT_CPU_RESET_EN                                            |
| 24  | LP_CLKRST_HPCOREO_LOCKUP_RESET_EN                                        |
| 23  | (reserved)                                                                |
| 22  | LP_CLKRST_CPU_RESET_LENGTH                                               |
| 21  | LP_CLKRST_CPU_RESET_EN                                                    |
| 20  | LP_CLKRST_RTC_WDT_CPU_RESET_LENGTH                                       |

LP_CLKRST_HPCOREO_LOCKUP_RESET_EN Configures the lockup reset enable setting for HP core0.
    0: Disable
    1: Enable (R/W)

LP_CLKRST_RTC_WDT_CPU_RESET_LENGTH Configures the length of RWDT CPU reset.
Measurement unit: LP_DYN_FAST_CLK clock cycles.
(R/W)

LP_CLKRST_RTC_WDT_CPU_RESET_EN Configures whether or not to enable RWDT CPU reset.
    0: Disable RWDT CPU reset.
    1: Enable RWDT CPU reset.
(R/W)

LP_CLKRST_CPU_STALL_WAIT Configure the time interval between CPU stall and reset.
Measurement unit: LP_DYN_FAST_CLK clock cycles.
(R/W)

LP_CLKRST_CPU_STALL_EN Configures whether or not CPU will stall before RWDT and software reset CPU.
    0: CPU will not stall.
    1: CPU will stall.
(R/W)

Register 7.69. LP_CLKRST_FOSC_CNTL_REG (0x0018)

| Bit | Description |
|-----|-------------|
| 31  | Oxac        |
| 22  | (reserved)  |

LP_CLKRST_FOSC_DFRQ Configures the frequency of RC_FAST_CLK frequency. (R/W)
```