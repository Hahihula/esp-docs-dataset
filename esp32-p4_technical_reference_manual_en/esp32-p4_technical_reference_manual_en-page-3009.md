

```markdown
Register 60.26. LP_ANA_TOUCH_MUXO_REG (0x013C)

Continued from the previous page...

LP_ANA_TOUCH_START_EN Configures whether to enable software to trigger the START signal to start the measurement.
    O: Disable
    1: Enable
    (R/W)

LP_ANA_TOUCH_START_FORCE Configures whether to generate the DONE signal to start a measurement.
    O: Not generate
    1: Generate
    (R/W)
```

```markdown
Register 60.27. LP_ANA_TOUCH_MUX1_REG (0x0140)

| 31 | 30 | 29 | ... | 15 | 14 | ... | 0 |
|----|----|----|-----|----|----|-----|---|
| O  | O  |    |     |    |    |     | Reset |

LP_ANA_TOUCH_START Configures whether to activate the 14 touch pins. Bit 1-14 corresponds to touch pin 1-14 respectively. Other bits are invalid.
    O: No effect
    1: Activate
    (R/W)

LP_ANA_TOUCH_XPD Configures whether to power up the 14 touch pins. Bit 1-14 corresponds to touch pin 1-14 respectively. Other bits are invalid.
    O: Not power up
    1: Power up
    (R/W)
```