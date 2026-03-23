

```markdown
## Register 9.45. RTC_CNTL_LOW_POWER_ST_REG (0x00C8)

RTC_CNTL_RDY_FOR_WAKEUP Indicates the RTC is ready to be triggered by any wakeup source.
(RO)

RTC_CNTL_MAIN_STATE_IN_IDLE Indicates the RTC state.

- 0: the chip can be either
    - in sleep modes.
    - entering sleep modes. In this case, wait until `RTC_CNTL_RDY_FOR_WAKEUP` bit is set, then you can wake up the chip.
    - exiting sleep mode. In this case, `RTC_CNTL_MAIN_STATE_IN_IDLE` will eventually become 1.

- 1: the chip is not in sleep modes (i.e. running normally).
(RO)

## Register 9.46. RTC_CNTL_PAD_HOLD_REG (0x0D00)
```

```markdown
RTC_CNTL_GPIO_PIN0_HOLD Sets the GPIO 0 to the holding state. (R/W)

RTC_CNTL_GPIO_PIN1_HOLD Sets the GPIO 1 to the holding state. (R/W)

RTC_CNTL_GPIO_PIN2_HOLD Sets the GPIO 2 to the holding state. (R/W)

RTC_CNTL_GPIO_PIN3_HOLD Sets the GPIO 3 to the holding state. (R/W)

RTC_CNTL_GPIO_PIN4_HOLD Sets the GPIO 4 to the holding state. (R/W)

RTC_CNTL_GPIO_PIN5_HOLD Sets the GPIO 5 to the holding state. (R/W)
```