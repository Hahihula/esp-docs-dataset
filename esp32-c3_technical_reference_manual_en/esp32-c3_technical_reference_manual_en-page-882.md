

```markdown
## Register 34.7. APB_SARADC_APB_ADC_ARB_CTRL_REG (0x0024)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 30-28| APB_SARADC_ADC_ARB_FIX_PRIORITY    | APB SARADC ADC ARB fixed priority.                                         |
| 27-25| APB_SARADC_ADC_ARB_WIFI_PRIORITY   | APB SARADC ADC ARB WIFI priority.                                          |
| 24-13| (reserved)                         |                                                                             |
| 12  | APB_SARADC_ADC_ARB_ARB_PRIORITY     | APB SARADC ADC ARB priority.                                               |
| 11  | APB_SARADC_ADC_ARB_ARB_GRANT_FORCE  | APB SARADC ADC ARB grant force.                                            |
| 10  | APB_SARADC_ADC_ARB_ARB_WIFI_FORCE   | APB SARADC ADC ARB WIFI force.                                             |
| 9-8  | (reserved)                         |                                                                             |
| 7    | APB_SARADC_ADC_ARB_APB_FORCE        | SAR ADC2 arbiter forces to enable DIG ADC controller.                      |
| 6    | APB_SARADC_ADC_ARB_WIFI_FORCE      | SAR ADC2 arbiter forces to enable PWDFT controller.                        |
| 5-4   | (reserved)                         |                                                                             |
| 3    | APB_SARADC_ADC_ARB_GRANT_FORCE       | ADC2 arbiter force grant.                                                  |
| 2    | APB_SARADC_ADC_ARB_APB_PRIORITY      | Set DIG ADC controller priority.                                           |
| 1    | APB_SARADC_ADC_ARB_WIFI_PRIORITY    | Set PWDFT controller priority.                                             |
| 0    | APB_SARADC_ADC_ARB_FIX_PRIORITY       | ADC2 arbiter uses fixed priority.                                         |

## Register 34.8. APB_SARADC_FILTER_CTRL_REG (0x0028)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 30-26| APB_SARADC_FILTER_RESET             | Reset SAR ADC1 filter.                                                     |
| 25-18| APB_SARADC_FILTER_CHANNELNO         | The filter channel for SAR ADC filter 0.                                   |
| 17-14| (reserved)                         |                                                                             |
| 13  | APB_SARADC_FILTER_CHANNEL1           | The filter channel for SAR ADC filter 1.                                   |
```