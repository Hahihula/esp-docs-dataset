

```markdown
Register 14.8. RTC_WDT_SWD_CONFIG_REG (0x001C)

| 31 | 30 | 29             | 28               | 27                | 26                 | 25                  | 24                   | 23                    | 22                     | 21                      | 20                       | 19                        | 18                         | 17                          | (reserved)             |
|----:|----:|----------------|-----------------|------------------|-------------------|--------------------|---------------------|----------------------|-----------------------|------------------------|-------------------------|--------------------------|---------------------------|----------------------------|--------------------------|
|    |    | RTC_WDT_SWD_FEED | RTC_WDT_SWD_DISABLE | RTC_WDT_SWD_SIGNAL_WIDTH | RTC_WDT_SWD_RST_FLAG_CLR | RTC_WDT_SWD_AUTO_FEED_EN |                           |                         |                         |                         |                         |                         |                         |                         |
| 0  | 0  |                |                  |                    |                   |                     | 300                 |                       |                         |                         |                         |                         |                         | Reset                      |

RTC_WDT_SWD_RESET_FLAG Represents whether the SWD generates a reset signal or not.
O: No
1: Yes
(RO)

RTC_WDT_SWD_AUTO_FEED_EN Configures this bit to enable to feed SWD automatically by hardware.
O: Disable
1: Enable
(R/W)

RTC_WDT_SWD_RST_FLAG_CLR Configures this bit to clear SWD reset flag.
O: Invalid
1: Clear the reset flag
(WT)

RTC_WDT_SWD_SIGNAL_WIDTH Configure the SWD signal length that output to analog circuit.
Measurement unit: LP_DYN_FAST_CLK (R/W)

RTC_WDT_SWD_DISABLE Configures this bit to disable the SWD.
O: Enable the SWD
1: Disable the SWD
(R/W)

RTC_WDT_SWD_FEED Configures this bit to feed the SWD.
O: Invalid
1: Feed SWD
(WT)
```