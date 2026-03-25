

```markdown
Register 14.8. RTC_WDT_SWD_CONFIG_REG (0x0020)

| 31 | 30 | 29           | 28               | 27                 | 26                  | 25                   | 24                    | 23                     | 22                      | 21                       | 20            | 19 | 18   | 17                         | (reserved)             |
|----:|----:|:-------------|:-----------------|:-------------------|:--------------------|:---------------------|:----------------------|:-----------------------|:------------------------|:-------------------------|:--------------|----:|----:--|:----------------------------|:------------------------|
|   0 |   0 | 300          |                 |                   | RTC_WDT_SWD_SIGNAL_WIDTH | RTC_WDT_SWD_RST_FLAG_CLR | RTC_WDT_SWD_AUTO_FEED_EN | RTC_WDT_SWD_DISABLE    | RTC_WDT_SWD_FEED        | RTC_WDT_SWD_RESET_FLAG   |
|    |    |              |                 |                   |                        |                      |                       |                       |                        |                         | Reset         |

RTC_WDT_SWD_RESET_FLAG  Represents the SWD whether or not generate the reset signal
0: No
1: Yes
(RO)

RTC_WDT_SWD_AUTO_FEED_EN  Configure this bit to enable to feed SWD automatically by hardware.
0: Disable
1: Enable
(R/W)

RTC_WDT_SWD_RST_FLAG_CLR  Configure this bit to clear SWD reset flag
0: Invalid
1: clear the reset flag
(WT)

RTC_WDT_SWD_SIGNAL_WIDTH  Configures the SWD signal length that outputs to the analog circuit.
Measurement unit: RTC_DYN_FAST_CLK
(R/W)

RTC_WDT_SWD_DISABLE  Configure this bit to disable the SWD.
0: Enable the SWD
1: Disable the SWD
(R/W)

RTC_WDT_SWD_FEED  Configure this bit to feed the SWD.
0: Invalid
1: Feed SWD
(WT)
```