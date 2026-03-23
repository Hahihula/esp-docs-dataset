

```markdown
Register 9.60. RTC_CNTL_GPIO_WAKEUP_REG (0x0110)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 23 | 22 | 20 | 19 | 17 | 16 | 14 | 13 | 11 | 10 | 8 | 7 | 6 | 5 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  |    |    |    |    |    |    |    |    |    |    |    |    | Reset |

RTC_CNTL_GPIO_WAKEUP_STATUS Indicates the RTC GPIO that woke up the chip, with Bit0 to Bit5 representing RTC GPIO 0 to RTC GPIO 5, respectively. For example, 010000 indicates it is the RTC GPIO 4 that woke up the chip. (RO)

RTC_CNTL_GPIO_WAKEUP_STATUS_CLR Clears the RTC GPIO wakeup flag. (R/W)

RTC_CNTL_GPIO_PIN_CLK_GATE Enables the RTC GPIO clock gate. (R/W)

RTC_CNTL_GPIO_PIN5_INT_TYPE Configures RTC GPIO 5 wakeup type.
0: disable wakeup by RTC GPIO
1: wake up the chip upon the rising edge
2: wake up the chip upon the falling edge
3: wake up the chip upon the rising edge or the failing edge
4: wake up the chip upon low level
5: wake up the chip upon high level
(R/W)

RTC_CNTL_GPIO_PIN4_INT_TYPE Configures RTC GPIO 4 wakeup type.
0: disable wakeup by RTC GPIO
1: wake up the chip upon the rising edge
2: wake up the chip upon the falling edge
3: wake up the chip upon the rising edge or the failing edge
4: wake up the chip upon low level
5: wake up the chip upon high level
(R/W)

RTC_CNTL_GPIO_PIN3_INT_TYPE Configures RTC GPIO 3 wakeup type.
0: disable wakeup by RTC GPIO
1: wake up the chip upon the rising edge
2: wake up the chip upon the failing edge
3: wake up the chip upon the rising edge or the failing edge
4: wake up the chip upon low level
5: wake up the chip upon high level
(R/W)

Continued on the next page...
```