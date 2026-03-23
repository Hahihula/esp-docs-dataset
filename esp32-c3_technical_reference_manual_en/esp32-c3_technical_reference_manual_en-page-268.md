

```markdown
Chapter 9 Low-power Management

Register 9.60. RTC_CNTL_GPIO_WAKEUP_REG (0x0110)

Continued from the previous page...

RTC_CNTL_GPIO_PIN2_INT_TYPE Configures RTC GPIO 2 wakeup type.
- 0: disable wakeup by RTC GPIO
- 1: wake up the chip upon the rising edge
- 2: wake up the chip upon the falling edge
- 3: wake up the chip upon the rising edge or the falling edge
- 4: wake up the chip upon low level
- 5: wake up the chip upon high level
(R/W)

RTC_CNTL_GPIO_PIN1_INT_TYPE Configures RTC GPIO 1 wakeup type.
- 0: disable wakeup by RTC GPIO
- 1: wake up the chip upon the rising edge
- 2: wake up the chip upon the falling edge
- 3: wake up the chip upon the rising edge or the falling edge
- 4: wake up the chip upon low level
- 5: wake up the chip upon high level
(R/W)

RTC_CNTL_GPIO_PINO_INT_TYPE Configures RTC GPIO 0 wakeup type.
- 0: disable wakeup by RTC GPIO
- 1: wake up the chip upon the rising edge
- 2: wake up the chip upon the falling edge
- 3: wake up the chip upon the rising edge or the falling edge
- 4: wake up the chip upon low level
- 5: wake up the chip upon high level
(R/W)

RTC_CNTL_GPIO_PIN5_WAKEUP_ENABLE Enables wakeup from RTC GPIO 5. (R/W)
RTC_CNTL_GPIO_PIN4_WAKEUP_ENABLE Enables wakeup from RTC GPIO 4. (R/W)
RTC_CNTL_GPIO_PIN3_WAKEUP_ENABLE Enables wakeup from RTC GPIO 3. (R/W)
RTC_CNTL_GPIO_PIN2_WAKEUP_ENABLE Enables wakeup from RTC GPIO 2. (R/W)
RTC_CNTL_GPIO_PIN1_WAKEUP_ENABLE Enables wakeup from RTC GPIO 1. (R/W)
RTC_CNTL_GPIO_PINO_WAKEUP_ENABLE Enables wakeup from RTC GPIO 0. (R/W)
```