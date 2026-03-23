

```markdown
Chapter 8 Reset and Clock

Register 8.79. LP_CLKRST_RESET_CAUSE_REG (0x0010)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 30  | (reserved)                   |
| 29  | (reserved)                   |
| 28  | (reserved)                   |
| ... | ...                          |
| 5   | LP_CLKRST_CORE0_RESET_CAUSE_CLR |
| 4   | RTC_CLKRST_RESET_CAUSE       |
| 3-0 | Reset                        |

RTC_CLKRST_RESET_CAUSE Represents the reset cause.
(RO)

LP_CLKRST_CORE0_RESET_CAUSE_CLR Configures whether or not to trigger the reset cause to
0x0
O: Invalid. No effect
1: Trigger the reset cause to 0x0
(WT)
```