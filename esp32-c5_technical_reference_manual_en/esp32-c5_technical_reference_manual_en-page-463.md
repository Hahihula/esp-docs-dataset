

```markdown
Register 9.99. LPPERI_RESET_EN_REG (0x0004)

| 31 | 30 | 29 | ... | 25 | 24 | 23 | ... | Reset |
|----:|----:|----:|-----:|----:|----:|----:|-----:|-------|
|   0 |   0 |   0 |  o   |   0 |   0 |   0 |  o   |       |

LPPERI_RNG_RESET_EN Configures whether to do software reset of the RNG Controller.
O: Not reset
1: Reset
(R/W)

LPPERI_EFUSE_RESET_EN Configures whether to do software reset of the eFuse Controller.
O: Not reset
1: Reset
(R/W)
```