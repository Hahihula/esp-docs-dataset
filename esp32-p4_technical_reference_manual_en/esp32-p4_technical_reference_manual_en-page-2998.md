

```markdown
Register 60.13. LP_ANA_TOUCH_SCAN_CTRL1_REG (0x0100)

| Bit Range | Description |
|-----------|-------------|
| 31        |             |
|           | LP_ANA_TOUCH_SHIELD_PAD_EN Configures whether to enable the moisture tolerance feature.<br>0: Disable<br>1: Enable<br>(R/W) |
| 17-16     | LP_ANA_TOUCH_INACTIVE_CONNECTION Configures whether to power up the touch pins involved in the measurement in scan mode.<br>0: Not power up<br>1: Power up<br>(R/W) |
|           | LP_ANA_TOUCH_SCAN_PAD_MAP Configures which touch pins to use in scan mode for measurement. Bit 1-14 corresponds to touch pin 1-14 respectively. Other bits are invalid.<br>0: No effect<br>1: Enable the touch pin<br>(R/W) |
|           | LP_ANA_TOUCH_XPD_WAIT Configures the power-up wait time after initiating a measurement.<br>(R/W) |

LP_ANA_TOUCH_SHIELD_PAD_EN
LP_ANA_TOUCH_INACTIVE_CONNECTION
LP_ANA_TOUCH_SCAN_PAD_MAP
LP_ANA_TOUCH_XPD_WAIT

0x04 0 O Reset
```