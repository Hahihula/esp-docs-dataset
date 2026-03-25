

```markdown
Register 16.8. RTC_WDT_SWD_CONFIG_REG (0x001C)

| 31 | 30 | 29                         | 20   | 19     | 18                  | 17                        |
|----|----|-----------------------------|------|--------|---------------------|---------------------------|
| O  | O  | 300                        | O    | O      | O                   | O                         |
| Reset | RTC_WDT_SWD_RESET_FLAG | RTC_WDT_SWD:disable | RTC_WDT_SWD_SIGNAL_WIDTH | RTC_WDT_SWD_RST_FLAG_CLR | RTC_WDT_SWD_AUTO_FEED_EN |

RTC_WDT_SWD_RESET_FLAG  Represents whether the SWD generates a reset signal or not.
0: No
1: Yes
(RO)

RTC_WDT_SWD_AUTO_FEED_EN  Configures this bit to enable to feed SWD automatically by hardware.
0: Disable
1: Enable
(R/W)

RTC_WDT_SWD_RST_FLAG_CLR  Configures this bit to clear SWD reset flag.
0: Invalid
1: Clear the reset flag (WT)

RTC_WDT_SWD_SIGNAL_WIDTH  Configure the SWD signal length that output to analog circuit.
Measurement unit: LP_DYN_FAST_CLK (R/W)

RTC_WDT_SWD_DISABLE  Configures this bit to disable the SWD.
0: Enable the SWD
1: Disable the SWD (R/W)

RTC_WDT_SWD_FEED  Configures this bit to feed the SWD.
0: Invalid
1: Feed SWD (WT)
```