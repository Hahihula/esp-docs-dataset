

```markdown
In contrast, the clock source of RWDT is derived directly from LP_DYN_SLOW_CLK (see details in Chapter 10 Reset and Clock).

MWDT and RWDT are enabled by setting the TIMG_WDT_EN and RTC_WDT_EN fields respectively. When enabled, the 32-bit counters of the watchdog will increment on each source clock cycle until the timeout value of the current stage is reached (i.e., timeout of the current stage). When this occurs, the current counter value is reset to zero and the next stage will become active. If a watchdog timer is fed by software, the timer will return to stage 0 and reset its counter value to zero. Software can feed a watchdog timer by writing any value to TIMG_WDTFEED_REG for MDWT and by writing 1 to RTC_WDT_FEED for RWDT.

### 17.2.2.2 Stages and Timeout Actions

Timer stages allow for a timer to have a series of different timeout values and corresponding timeout action. When one stage times out, the timeout action is triggered, the counter value is reset to zero, and the next stage becomes active.

MWDT/RWDT offers four stages (referred to as stages 0 to 3). The watchdog timers will progress through each stage in a loop (i.e., from stage 0 to 3, then back to stage 0).

Timeout values of each stage for MWDT are configured in TIMG_WDTCONFIGI_REG (where i ranges from 2 to 5), whilst timeout values for RWDT are configured using RTC_WDT_STGj_HOLD field (where j ranges from 0 to 3).

Please note that the timeout value of stage 0 for RWDT ($Thold_0$) is determined by the combination of the EFUSE_WDT_DELAY_SEL field of eFuse register EFUSE_RD_REPEAT_DATA0_REG and RTC_WDT_STGO_HOLD field. The relationship is as follows:

$$
Thold_0 = RTC\_WDT\_STG0\_HOLD << (EFUSE\_WDT\_DELAY\_SEL + 1)
$$

where << is a left-shift operator. For example, if RTC_WDT_STGO_HOLD is configured as 100 and EFUSE_WDT_DELAY_SEL is 1, the $Thold_0$ will be 400 cycles.

Upon the timeout of each stage, one of the following timeout actions will be executed:

**Table 17.2-1. Timeout Actions**

| Timeout Action | Description |
|----------------|-------------|
| Interrupt      | Trigger an interrupt |
| HP CPU reset   | Reset the HP CPU0 and HP CPU1 |
| HP core reset  | HP core reset resets HP CPU0, HP CPI1, HP peripherals, HP GPIO, etc. |
| System reset   | Reset the whole digital system, including the LP system. |
| Disabled       | No effect on the system |

For MWDT, the timeout action of all stages is configured in TIMG_WDTCONFIG0_REG. Likewise for RWDT, the timeout action is configured in RTC_WDT_CONFIG0_REG.
```