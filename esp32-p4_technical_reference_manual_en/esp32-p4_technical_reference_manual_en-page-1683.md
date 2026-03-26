

```markdown
Register 36.22. ISP_DEMOSAIC_GRAD_RATIO_REG (0x005C)

| 31 | (reserved) | 6 | 5 | 0 |
|-----|------------|---|---|---|
| 0   |            | 0 | 0 | 16 | Reset |

ISP_DEMOSAIC_GRAD_RATIO Configures the demosaic effect, with bits [5:4] as the integer part and bits [3:0] as the fractional part. (R/W)

Register 36.23. ISP_GAMMA_CTRL_REG (0x0074)

| 31 | (reserved) | 4 | 3 | 2 | 1 | 0 |
|-----|------------|---|---|---|---|---|
| 0   |            | 0 | 0 | 1 | 1 | 0 | Reset |

ISP_GAMMA_UPDATE Configures whether to update the gamma curve parameters. Writing 1 to this field updates the gamma curve parameters. It will be automatically cleared to 0 after the update is complete. (R/W)

ISP_GAMMA_B_LAST_CORRECT Configures whether to enable correction for the parameters of the last interval on the X axis of B channel gamma curve.
O: Not enable
1: Enable
(R/W)

ISP_GAMMA_G_LAST_CORRECT Configures whether to enable correction for the parameters of the last interval on the X axis of G channel gamma curve.
O: Not enable
1: Enable
(R/W)

ISP_GAMMA_R_LAST_CORRECT Configures whether to enable correction for the parameters of the last interval on the X axis of X channel gamma curve.
O: Not enable
1: Enable
(R/W)
```