

```markdown
Register 62.1. ADC_CTRL_REG (0x0000)

Continued from the previous page...

ADC_XPD_SAR1_FORCE Keep HP ADC1 powered on forcefully.
O: No effect
1: Power on forcefully
(R/W)

ADC_XPD_SAR2_FORCE Keep HP ADC2 powered on forcefully.
O: No effect
1: Power on forcefully
(R/W)

Register 62.2. ADC_CTRL2_REG (0x0004)


| 31 | 25 | 24 | 23 | 12 | 11 | 10 | 9 | 8 | 1 | 0 |
|----|----|----|----|----|----|----|---|---|---|---|
|    | (reserved) | ADC_TIMER_EN | ADC_TIMER_TARGET | (reserved) | ADC_SAR2_INV | ADC_MAX_MEAS_NUM | ADC_MEAS_NUM_LIMIT | Reset |

ADC_MEAS_NUM_LIMIT Configures whether to enable the limitation of HP ADC's maximum conversion times.
O: Disable
1: Enable
(R/W)

ADC_MAX_MEAS_NUM Configures the HP ADC's maximum conversion times. (R/W)

ADC_SAR1_INV Configures whether to invert the data of HP ADC1.
O: Do not invert.
1: Invert the date.
(R/W)

ADC_SAR2_INV Configures whether to to invert the data of HP ADC2.
O: Do not invert.
1: Invert the date.
(R/W)

ADC_TIMER_TARGET Configures HP ADC timer target. (R/W)

ADC_TIMER_EN Configures whether to enable HP ADC timer trigger.
O: Disable
1: Enable
(R/W)
```