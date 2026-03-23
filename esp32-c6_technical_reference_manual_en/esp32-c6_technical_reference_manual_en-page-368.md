

```markdown
Register 8.78. LP_CLKRST_LP_RST_EN_REG (0x000C)
```

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | LP_CLKRST_ANA_PERI_RESET_EN                                                |
| 30  | LP_CLKRST_WDT_RESET_EN                                                     |
| 29  | LP_CLKRST_RTC_TIMER_RESET_EN                                               |
| 28  | LP_CLKRST_AON_EFUSE_CORE_RESET_EN                                          |
|     | (reserved)                                                                 |

```markdown
LP_CLKRST_AON_EFUSE_CORE_RESET_EN Configures whether or not to reset EFUSE_CTRL always-on part

0: Invalid.No effect<br>
1: Reset<br>
(R/W)
```

```markdown
LP_CLKRST_RTC_TIMER_RESET_EN Configures whether or not to reset RTC_TIMER

0: Invalid.No effect<br>
1: Reset<br>
(R/W)
```

```markdown
LP_CLKRST_WDT_RESET_EN Configures whether or not to reset RTC_WDT and super watch dog

0: Invalid.No effect<br>
1: Reset<br>
(R/W)
```

```markdown
LP_CLKRST_ANA_PERI_RESET_EN Configures whether or not to reset analog peri, include brownout controller

0: Invalid.No effect<br>
1: Reset<br>
(R/W)
```
```