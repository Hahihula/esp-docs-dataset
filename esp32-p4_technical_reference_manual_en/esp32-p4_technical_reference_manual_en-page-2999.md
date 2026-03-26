

```markdown
Register 60.14. LP_ANA_TOUCH_SCAN_CTRL2_REG (0x0104)

| Bit | Description                        |
|-----|------------------------------------|
| 31  | (reserved)                         |
| 30  | LP_ANA_FREQ_SCAN_CNT_LIMIT         |
| 29  | LP_ANA_FREQ_SCAN_EN                |
| 28  | LP_ANA_TOUCH_OUT_RING              |
| 27  | LP_ANA_TOUCH_TIMEOUT_EN            |
| 26  | LP_ANA_TOUCH_TIMEOUT_NUM           |
| 23..21 | (reserved)                     |
| 6   | (reserved)                         |
| 5   | (reserved)                         |
| 0   | Reset                              |

LP_ANA_TOUCH_TIMEOUT_NUM Configures the number of measurement timeouts. (R/W)

LP_ANA_TOUCH_TIMEOUT_EN Configures whether to enable the measurement timeout.
O: Disable
1: Enable
(R/W)

LP_ANA_TOUCH_OUT_RING Configures which touch pins to be used for water rejection. Configurable values are 1-14. Other values are invalid. (R/W)

LP_ANA_FREQ_SCAN_EN Configures whether to enable frequency hopping.
O: Disable
1: Enable
(R/W)

LP_ANA_FREQ_SCAN_CNT_LIMIT Configures the number of frequency hops.
O: 1
1: 2
2: 3
3: Invalid
(R/W)
```