

```markdown
Register 60.25. LP_ANA_TOUCH_ANA_PARA_REG (0x0138)
```

| Bit | Description |
|-----|-------------|
| 31-11 | (reserved) |
| 10   | LP_ANA_TOUCH_TOUCH_DCAP_CAL |
| 9    | LP_ANA_TOUCH_TOUCH_EN_CAL |
| 8    | LP_ANA_TOUCH_TOUCH_BUF_DRV |

LP_ANA_TOUCH_TOUCH_BUF_DRV Configures the value of BUF_DRV. (R/W)

LP_ANA_TOUCH_TOUCH_EN_CAL Configures whether to enable the touch sensor internal capacitance test mode.
- 0: Disable
- 1: Enable
(R/W)

LP_ANA_TOUCH_TOUCH_DCAP_CAL Configures the internal capacitance connected to the touch pins. The default value is 0, and the adjustment range is 0-127 pF with a step of 1. (R/W)
```