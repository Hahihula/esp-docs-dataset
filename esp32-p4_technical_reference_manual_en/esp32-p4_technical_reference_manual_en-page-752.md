

```markdown
Register 10.64. LP_CLKRST_HPCPU_RESET_CTRL1_REG (0x0018)

| 31 | 24 | 23 | 16 | 15 |
|-----|-----|-----|----|----|
| 0x0 |     | LP_CLKRST_HPCORE1_SW_STALL_CODE | 0 0 0 0 0 0 0 0 | (reserved) |
|     |     |                             |                  |            |

LP_CLKRST_HPCOREO_SW_STALL_CODE Configures the threshold for HP CPU0 stall triggered by software. (R/W)

LP_CLKRST_HPCORE1_SW_STALL_CODE Configures the threshold for HP CPU1 stall triggered by software. (R/W)


Register 10.65. LP_CLKRST_FOSC_CNTL_REG (0x001C)

| 31 | 22 | 21 |
|----|----|----|
| 400 |    |    |
|     | 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | (reserved) |

LP_CLKRST_FOSC_DFreq Configures the frequency of RC_FAST_CLK. (R/W)
```