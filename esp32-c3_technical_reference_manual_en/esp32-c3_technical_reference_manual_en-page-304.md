

```markdown
Register 11.26. TIMG_REGCLK_REG (0x00FC)
```

| Bit | 31 | 30 | 29 | 28 | ... | 0 |
|-----|----|----|----|----|-----|---|
|     | TIMG_CLK_EN | TIMG_TIMER_CLK_IS_ACTIVE | TIMG_WDT_CLK_IS_ACTIVE | (reserved) |         | Reset |

```markdown
TIMG_WDT_CLK_IS_ACTIVE enable WDT’s clock (R/W)

TIMG_TIMER_CLK_IS_ACTIVE enable Timer 0’s clock (R/W)

TIMG_CLK_EN Register clock gate signal. 0: The clock used by software to read and write registers is on only when there is software operation. 1: The clock used by software to read and write registers is always on. (R/W)
```