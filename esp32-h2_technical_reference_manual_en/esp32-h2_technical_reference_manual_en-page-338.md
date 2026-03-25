

```markdown
Register 7.81. LP_CLKRST_RESET_CAUSE_REG (0x0010)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | LP_CLKRST_COREO_RESET_FLAG_CLR                                            |
| 30  | LP_CLKRST_COREO_RESET_FLAG_SET                                           |
| 29  | LP_CLKRST_COREO_RESET_CAUSE_CLR                                          |
|     | (reserved)                                                                 |
| 6   | LP_CLKRST_COREO_RESET_FLAG                                               |
| 5   | LP_CLKRST_COREO_RESET_FLAG_SET                                           |
| 4   | LP_CLKRST_COREO_RESET_CAUSE_CLR                                          |
| 3   | LP_CLKRST_COREO_RESET_FLAG_SET                                          |
| 2   | LP_CLKRST_COREO_RESET_FLAG_CLR                                          |
| 1   | Reset                                                                     |
| 0   | Reset                                                                     |

RTC_CLKRST_RESET_CAUSE Represents the reset cause. (RO)

LP_CLKRST_COREO_RESET_FLAG Represents whether the reset occurred is recorded in LP_CLKRST_RESET_CAUSE.
- 0: Illegal reset
- 1: Recorded reset
(RO)

LP_CLKRST_COREO_RESET_CAUSE_CLR Write 1 to clear LP_CLKRST_RESET_CAUSE. (WT)

LP_CLKRST_COREO_RESET_FLAG_SET Write 1 to set LP_CLKRST_COREO_RESET_FLAG. (WT)

LP_CLKRST_COREO_RESET_FLAG_CLR Write 1 to clear LP_CLKRST_COREO_RESET_FLAG. (WT)
```