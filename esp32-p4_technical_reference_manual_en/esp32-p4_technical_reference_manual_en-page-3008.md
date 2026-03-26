

```markdown
Register 60.26. LP_ANA_TOUCH_MUXO_REG (0x013C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|-----|----|----|----|---|---|---|---|---|---|---|---|---|---|
|     |    |    |    |    |    |    |      |    |    |    |   |   |   |   |   |   |   |   |   |   |
| Value | 0 | 1 | 0 | 0 | O | (reserved) | Reset |

LP_ANA_TOUCH_DATA_SEL Configures the type of the return value.
- 0/1: touch_raw_data
- 2: benchmark
- 3: touch_smooth_data
(R/W)

LP_ANA_TOUCH_FREQ_SEL Configures the corresponding sampling frequency mode of the return value.
- 0: 0
- 1: 1
- 2: 2
- 3: Invalid
(R/W)

LP_ANA_TOUCH_BUFSEL Configures whether to enable a touch pin to be used for moisture tolerance. Bit 1-14 corresponds to touch pin 1-14 respectively. Other bits are invalid.
- 0: Disable
- 1: Enable
(R/W)

LP_ANA_TOUCH_DONE_EN Configures whether to enable software to trigger the DONE signal that enables the measurement.
- 0: Disable
- 1: Enable
(R/W)

LP_ANA_TOUCH_DONE_FORCE Configures whether to generate the DONE signal to end the current measurement operation.
- 0: Not generate
- 1: Generate
(R/W)

LP_ANA_TOUCH_FSM_EN Configures the control source to power up and activate touch pins.
- 0: Controlled by software
- 1: Controlled by hardware
(R/W)
```
Continued on the next page...
```