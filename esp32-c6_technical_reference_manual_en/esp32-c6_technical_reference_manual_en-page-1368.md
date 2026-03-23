

```markdown
Register 39.1. APB_SARADC_CTRL_REG (0x0000)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | APB_SARADC_WAIT_ARB_CYCLE                                                   |
| 30  | (reserved)                                                                  |
| 29  | APB_SARADC_XPD_SAR_FORCE                                                    |
| 28  | (reserved)                                                                  |
| 27  | APB_SARADC_SAR_PATT_P_CLEAR                                                 |
| 26  | (reserved)                                                                  |
| 25  | APB_SARADC_SAR_PATT_LEN                                                     |
| 24  | APB_SARADC_SAR_CLK_GATED                                                    |
| 23  | APB_SARADC_SAR_CLK_DIV                                                      |
| 22  | APB_SARADC_START_FORCE                                                      |
| 21  | APB_SARADC_START                                                              |
| 20  | (reserved)                                                                  |
| 19  | (reserved)                                                                  |
| 18  | (reserved)                                                                  |
| 17  | (reserved)                                                                  |
| 16  | (reserved)                                                                  |
| 15  | (reserved)                                                                  |
| 14  | (reserved)                                                                  |
| 13  | (reserved)                                                                  |
| 12  | (reserved)                                                                  |
| 11  | (reserved)                                                                  |
| 10  | (reserved)                                                                  |
| 9   | (reserved)                                                                  |
| 8   | (reserved)                                                                  |
| 7   | (reserved)                                                                  |
| 6   | (reserved)                                                                  |
| 5   | (reserved)                                                                  |
| 4   | (reserved)                                                                  |
| 3   | (reserved)                                                                  |
| 2   | (reserved)                                                                  |
| 1   | (reserved)                                                                  |
| 0   | Reset                                                                       |

APB_SARADC_START_FORCE Configures whether to use software to enable SAR ADC.
- 0: Select FSM to start SAR ADC
- 1: Select software to start SAR ADC
(R/W)

APB_SARADC_START Configures whether to start SAR ADC by software.
- 0: No effect
- 1: Start SAR ADC by software
Valid only when APB_SARADC_START_FORCE = 1.
(R/W)

APB_SARADC_SAR_CLK_GATED Configures whether to enable SAR ADC clock gate.
- 0: Disable
- 1: Enable
(R/W)

APB_SARADC_SAR_CLK_DIV Configures SAR ADC clock divider. This value should be no less than 2.
(R/W)

APB_SARADC_SAR_PATT_LEN Configures how many pattern table entries will be used.
- 0: Only cmd3 will be used
- 1: Pattern table entries cmd0 and cmd1 will be used
(R/W)

APB_SARADC_SAR_PATT_P_CLEAR Configures whether to clear the pointer of pattern table for DIG ADC controller.
- 0: No effect
- 1: Clear
(R/W)

APB_SARADC_XPD_SAR_FORCE Configures whether to force select XPD SAR.
- 0: No effect
- 1: Force select XPD SAR
(R/W)

APB_SARADC_WAIT_ARB_CYCLE Configures the clock cycle of waiting arbitration signal stable after SAR_DONE. (R/W)
```