

```markdown
## Register 9.91. LP_CLKRST_CPU_RESET_REG (0x0014)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | LP_CLKRST_CPU_STALL_EN                 | Configures whether or not CPU will stall before RWDT and software reset CPU. O: CPU will not stall.<br>1: CPU will stall. (R/W) |
| 30  | LP_CLKRST_CPU_STALL_WAIT               | Configure the time interval between CPU stall and reset.<br>Measurement unit: LP_DYN_FAST_CLK clock cycles. (R/W) |
| 26  | LP_CLKRST_RTC_WDT_CPU_RESET_LENGTH    | Configures the length of RWDT CPU reset.<br>Measurement unit: LP_DYN_FAST_CLK clock cycles. (R/W) |
| 25  | LP_CLKRST_RTC_WDT_CPU_RESET_EN         | Configures whether or not to enable RWDT CPU reset.<br>0: Enable RWDT CPU reset.<br>1: Disable RWDT CPU reset. (R/W) |
| 24  | LP_CLKRST_CPU_STALL_EN                 | Configures whether or not CPU will stall before RWDT and software reset CPU. O: CPU will not stall.<br>1: CPU will stall. (R/W) |
| 23  | LP_CLKRST_RTC_WDT_CPU_RESET_LENGTH     | Configures the length of RWDT CPU reset.<br>Measurement unit: LP_DYN_FAST_CLK clock cycles. (R/W) |
| 22  | LP_CLKRST_CPU_STALL_WAIT               | Configure the time interval between CPU stall and reset.<br>Measurement unit: LP_DYN_FAST_CLK clock cycles. (R/W) |
| 21  | (reserved)                             |                                                                             |

LP_CLKRST_RTC_WDT_CPU_RESET_LENGTH Configures the length of RWDT CPU reset.
Measurement unit: LP_DYN_FAST_CLK clock cycles.
(R/W)

LP_CLKRST_RTC_WDT_CPU_RESET_EN Configures whether or not to enable RWDT CPU reset.
0: Enable RWDT CPU reset.
1: Disable RWDT CPU reset.
(R/W)

LP_CLKRST_CPU_STALL_WAIT Configure the time interval between CPU stall and reset.
Measurement unit: LP_DYN_FAST_CLK clock cycles.
(R/W)

LP_CLKRST_CPU_STALL_EN Configures whether or not CPU will stall before RWDT and software reset CPU.
O: CPU will not stall.
1: CPU will stall.
(R/W)
```

```markdown
## Register 9.92. LP_CLKRST_FOSC_CNTL_REG (0x0018)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | LP_CLKRST_FOSC_DFREQ                   | Configures the frequency of RC_FAST_CLK frequency. (R/W)                     |

LP_CLKRST_FOSC_DFREQ Configures the frequency of RC_FAST_CLK frequency. (R/W)
```