

```markdown
Register 7.86. LP_CLKRST_LPPERI_REG (0x0028)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | LP_CLKRST_LP_SEL_XTAL32K                   | Configures the clock source for RTC BLE Timer.                              |
| 29  | LP_CLKRST_LP_SEL_XTAL                      | Selects XTAL_CLK as the source clock for RTC BLE Timer. (R/W)               |
| 28  | LP_CLKRST_LP_SEL_OSC_FAST                  | Selects RC_FAST_CLK as the source clock for RTC BLE Timer. (R/W)            |
| 27  | LP_CLKRST_LP_SEL_OSC_SLOW                  | Selects RC_SLOW_CLK as the source clock for RTC BLE Timer. (R/W)            |
| 26  | LP_CLKRST_LP_BLETIMER_DIV_NUM             | Configures the divisor of the clock divider for RTC BLE Timer.              |
| 25  | (reserved)                                 |                                                                             |
| 24  | (reserved)                                 |                                                                             |
| 23  | (reserved)                                 |                                                                             |
| 12  | LP_CLKRST_LP_BLETIMER_DIV_NUM             | The working clock frequency of RTC BLE Timer is equal to the source clock frequency divided by ((LP_CLKRST_LP_BLETIMER_DIV_NUM - 1) / 2). (R/W) |

LP_CLKRST_LP_SEL_OSC_SLOW Configures the clock source for RTC BLE Timer.
- 1: Selects RC_SLOW_CLK as the source clock for RTC BLE Timer.
- 0: Disables RC_SLOW_CLK as the source clock for RTC BLE Timer. (R/W)

LP_CLKRST_LP_SEL_OSC_FAST Configures the clock source for RTC BLE Timer.
- 1: Selects RC_FAST_CLK as the source clock for RTC BLE Timer.
- 0: Disables RC_FAST_CLK as the source clock for RTC BLE Timer. (R/W)

LP_CLKRST_LP_SEL_XTAL Configures the clock source for RTC BLE Timer.
- 1: Selects XTAL_CLK as the source clock for RTC BLE Timer.
- 0: Disables XTAL_CLK as the source clock for RTC BLE Timer. (R/W)

LP_CLKRST_LP_SEL_XTAL32K Configures the clock source for RTC BLE Timer.
- 1: Selects XTAL32K_CLK as the source clock for RTC BLE Timer.
- 0: Disables XTAL32K_CLK as the source clock for RTC BLE Timer. (R/W)

Register 7.87. LP_CLKRST_XTAL32K_REG (0x002C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | LP_CLKRST_DRES_XTAL32K                     | Configures DRES (R/W)                                                        |
| 29  | LP_CLKRST_DGM_XTAL32K                      | Configures DGM (R/W)                                                         |
| 28  | LP_CLKRST_DBUF_XTAL32K                     | Configures DBUF (R/W)                                                        |
| 27  | LP_CLKRST_DAC_XTAL32K                      | Configures DAC (R/W)                                                         |
```