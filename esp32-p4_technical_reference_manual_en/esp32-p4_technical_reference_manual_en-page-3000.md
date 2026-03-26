

```markdown
Register 60.15. LP_ANA_TOUCH_WORK_REG (0x0108)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | LP_ANA_TOUCH_OUT_GATE | LP_ANA_DIV_NUMO | LP_ANA_DIV_NUM1 | LP_ANA_DIV_NUM2 | (reserved) | LP_ANA_TOUCH_OUT_SEL | LP_ANA_TOUCH_OUT_GATE | (reserved) |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0x0 | 0x0 | Reset |

LP_ANA_DIV_NUM2 Configures the enabling of the TOUCH_OUT signal division and the coefficient for sampling frequency mode 0.
bit[0]: Configures whether to enable division.
O: Disable
1: Enable
bit[1-2]: Configures the TOUCH_OUT signal division coefficient.
O: 0
1: 2
2: 4
3: 6
(R/W)

LP_ANA_DIV_NUM1 Configures the enabling of the TOUCH_OUT signal division and the coefficient for sampling frequency mode 1. For detailed configuration, refer to LP_ANA_DIV_NUM2. (R/W)

LP_ANA_DIV_NUMO Configures the enabling of the TOUCH_OUT signal division and the coefficient for sampling frequency mode 2. For detailed configuration, refer to LP_ANA_DIV_NUM2. (R/W)

LP_ANA_TOUCH_OUT_SEL Configures whether to use the TOUCH_OUT signal for clock or data.
O: TOUCH_OUT signal is used as data
1: TOUCH_OUT signal is used as clock
(R/W)

LP_ANA_TOUCH_OUT_GATE Configures whether to enable gating after enabling the TOUCH_OUT signal division.
O: Disable
1: Enable
(R/W)
```