

```markdown
Register 14.70. PMU_SDIO_WAKEUP_CNTL_REG (0x01F8)

PMU_SDIO_ACT_DNUM Configures the duration for maintaining the working state of SDIO. The unit is LP_DYN_FAST_CLK. (R/W)


Register 14.71. PMU_TOUCH_PWR_CNTL_REG (0x0210)

PMU_TOUCH_WAIT_CYCLES Configures the waiting time for the PMU to wake up from the TOUCH timer, with the unit of LP_DYN_SLOW_CLK. (R/W)
PMU_TOUCH_SLEEP_CYCLES Configure the sleep time for TOUCH, with the unit of LP_DYN_SLOW_CLK. (R/W)
PMU_TOUCH_FORCE_DONE Force return to the working state of the TOUCH timer. (R/W)
PMU_TOUCH_SLEEP_TIMER_EN Enables the TOUCH timer to start working. (R/W)


Register 14.72. PMU_DATE_REG (0x03FC)

PMU_PMU_DATE Version control register. (R/W)
PMU_CLK_EN Force enables the automatic clock gating of the register. (R/W)
```