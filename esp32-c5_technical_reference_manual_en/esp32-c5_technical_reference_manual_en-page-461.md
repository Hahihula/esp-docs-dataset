

```markdown
Register 9.95. LP_CLKRST_LPPERI_REG (0x0028)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | LP_CLKRST_LP_SEL_XTAL32K                   | Configures the clock source for RTC BLE Timer.                              |
| 29  | LP_CLKRST_LP_SEL_XTAL                      | The working clock frequency of RTC BLE Timer is equal to the source clock frequency divided by ((LP_CLKRST_LP_BLETIMER_DIV_NUM - 1) / 2). (R/W) |
| 28  | LP_CLKRST_LP_SEL_OSC_FAST                  | Selects RC_FAST_CLK as the source clock for RTC BLE Timer.                 |
| 27  | LP_CLKRST_LP_SEL_OSC_SLOW                  | Selects RC_SLOW_CLK as the source clock for RTC BLE Timer.                 |
| 26  | LP_CLKRST_LP_SEL_XTAL                      | Selects XTAL_CLK as the source clock for RTC BLE Timer.                    |
| 25  | LP_CLKRST_LP_SEL_XTAL32K                   | Selects XTAL32K_CLK as the source clock for RTC BLE Timer.                 |
| 24  | (reserved)                                 |                                                                             |
| 23  | (reserved)                                 |                                                                             |
| 12  | LP_CLKRST_LP_BLETIMER_DIV_NUM             | Configures the divisor of the clock divider for RTC BLE Timer.              |
| 11  | (reserved)                                 |                                                                             |
| 10  | (reserved)                                 |                                                                             |
| 9   | (reserved)                                 |                                                                             |
| 8   | (reserved)                                 |                                                                             |
| 7   | (reserved)                                 |                                                                             |
| 6   | (reserved)                                 |                                                                             |
| 5   | (reserved)                                 |                                                                             |
| 4   | (reserved)                                 |                                                                             |
| 3   | (reserved)                                 |                                                                             |
| 2   | (reserved)                                 |                                                                             |
| 1   | (reserved)                                 |                                                                             |
| 0   | Reset                                      |                                                                             |

LP_CLKRST_LP_BLETIMER_DIV_NUM Configures the divisor of the clock divider for RTC BLE Timer. The working clock frequency of RTC BLE Timer is equal to the source clock frequency divided by ((LP_CLKRST_LP_BLETIMER_DIV_NUM - 1) / 2). (R/W)

LP_CLKRST_LP_SEL_OSC_SLOW Configures the clock source for RTC BLE Timer.
1: Selects RC_SLOW_CLK as the source clock for RTC BLE Timer.
0: Disables RC_SLOW_CLK as the source clock for RTC BLE Timer. (R/W)

LP_CLKRST_LP_SEL_OSC_FAST Configures the clock source for RTC BLE Timer.
1: Selects RC_FAST_CLK as the source clock for RTC BLE Timer.
0: Disables RC_FAST_CLK as the source clock for RTC BLE Timer. (R/W)

LP_CLKRST_LP_SEL_XTAL Configures the clock source for RTC BLE Timer.
1: Selects XTAL_CLK as the source clock for RTC BLE Timer.
0: Disables XTAL_CLK as the source clock for RTC BLE Timer. (R/W)

LP_CLKRST_LP_SEL_XTAL32K Configures the clock source for RTC BLE Timer.
1: Selects XTAL32K_CLK as the source clock for RTC BLE Timer.
0: Disables XTAL32K_CLK as the source clock for RTC BLE Timer. (R/W)
```

```markdown
Register 9.96. LP_CLKRST_XTAL32K_REG (0x002C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | LP_CLKRST_DRES_XTAL32K                     | Configures DRES (R/W)                                                       |
| 29  | LP_CLKRST_DGM_XTAL32K                      | Configures DGM (R/W)                                                        |
| 28  | LP_CLKRST_DBUF_XTAL32K                     | Configures DBUF (R/W)                                                       |
| 27  | LP_CLKRST_DAC_XTAL32K                      | Configures DAC (R/W)                                                        |
| 26  | (reserved)                                 |                                                                             |
| 25  | (reserved)                                 |                                                                             |
| 24  | (reserved)                                 |                                                                             |
| 23  | (reserved)                                 |                                                                             |
| 22  | (reserved)                                 |                                                                             |
| 21  | (reserved)                                 |                                                                             |
| 20  | (reserved)                                 |                                                                             |
| 19  | (reserved)                                 |                                                                             |
| 18  | (reserved)                                 |                                                                             |
| 17  | (reserved)                                 |                                                                             |
| 16  | (reserved)                                 |                                                                             |
| 15  | (reserved)                                 |                                                                             |
| 14  | (reserved)                                 |                                                                             |
| 13  | (reserved)                                 |                                                                             |
| 12  | (reserved)                                 |                                                                             |
| 11  | (reserved)                                 |                                                                             |
| 10  | (reserved)                                 |                                                                             |
| 9   | (reserved)                                 |                                                                             |
| 8   | (reserved)                                 |                                                                             |
| 7   | (reserved)                                 |                                                                             |
| 6   | (reserved)                                 |                                                                             |
| 5   | (reserved)                                 |                                                                             |
| 4   | (reserved)                                 |                                                                             |
| 3   | (reserved)                                 |                                                                             |
| 2   | (reserved)                                 |                                                                             |
| 1   | (reserved)                                 |                                                                             |
| 0   | Reset                                      |                                                                             |

LP_CLKRST_DRES_XTAL32K Configures DRES (R/W)
LP_CLKRST_DGM_XTAL32K Configures DGM (R/W)
LP_CLKRST_DBUF_XTAL32K Configures DBUF (R/W)
LP_CLKRST_DAC_XTAL32K Configures DAC (R/W)
```