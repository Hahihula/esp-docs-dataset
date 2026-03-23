

```markdown
Register 34.1. APB_SARADC_CTRL_REG (0x0000)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | APB_SARADC_WAIT_ARB_CYCLE                                                 | reserved)
| 30  | APB_SARADC_XPD_SAR_FORCE                                                  | (reserved)
| 29  | APB_SARADC_START_FORCE                                                    | (reserved)
| 28  | APB_SARADC_SAR_PATT_LEN                                                   | (reserved)
| 27  | APB_SARADC_SAR_PATT_P_CLEAR                                               | reserved)
| 26  | APB_SARADC_SAR_CLK_DIV                                                    | reserved)
| 25  | APB_SARADC_SAR_CLK_GATED                                                  | reserved)
| 24  | APB_SARADC_START                                                           | reserved)
| 23  | APB_SARADC_START_FORCE                                                     | (reserved)
| 22  | APB_SARADC_START                                                           | (reserved)
| 21  | APB_SARADC_START                                                           | (reserved)
| 20  | APB_SARADC_START                                                           | (reserved)
| 19  | APB_SARADC_START                                                           | (reserved)
| 18  | APB_SARADC_START                                                           | (reserved)
| 17  | APB_SARADC_START                                                           | (reserved)
| 16  | APB_SARADC_START                                                           | (reserved)
| 15  | APB_SARADC_START                                                           | (reserved)
| 14  | APB_SARADC_START                                                           | (reserved)
| 13  | APB_SARADC_START                                                           | (reserved)
| 12  | APB_SARADC_START                                                           | (reserved)
| 11  | APB_SARADC_START                                                           | (reserved)
| 10  | APB_SARADC_START                                                           | (reserved)
| 9   | APB_SARADC_START                                                           | (reserved)
| 8   | APB_SARADC_START                                                           | (reserved)
| 7   | APB_SARADC_START                                                           | (reserved)
| 6   | APB_SARADC_START                                                           | (reserved)
| 5   | APB_SARADC_START                                                           | (reserved)
| 4   | APB_SARADC_START                                                           | (reserved)
| 3   | APB_SARADC_START                                                           | (reserved)
| 2   | APB_SARADC_START                                                           | (reserved)
| 1   | APB_SARADC_START                                                           | (reserved)
| 0   | Reset                                                                     |

APB_SARADC_START_FORCE O: select FSM to start SAR ADC. 1: select software to start SAR ADC.
(R/W)

APB_SARADC_START Write 1 here to start the SAR ADC by software. Valid only when APB_SARADC_START_FORCE = 1. (R/W)

APB_SARADC_SAR_CLK_GATED SAR ADC clock gate enable bit. (R/W)

APB_SARADC_SAR_CLK_DIV SAR ADC clock divider. This value should be no less than 2. (R/W)

APB_SARADC_SAR_PATT_LEN Configure how many pattern table entries will be used. If this field is set to 1, then pattern table entries (cmd0) and (cmd1) will be used. (R/W)

APB_SARADC_SAR_PATT_P_CLEAR Clear the pointer of pattern table entry for DIG ADC controller.
(R/W)

APB_SARADC_XPD_SAR_FORCE Force select XPD SAR. (R/W)

APB_SARADC_WAIT_ARB_CYCLE The clock cycles of waiting arbitration signal stable after SAR_DONE. (R/W)
```