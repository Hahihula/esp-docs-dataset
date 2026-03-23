

```markdown
When enabled, the 32-bit counters of each watchdog will increment on each source clock cycle until the timeout value of the current stage is reached (i.e. expiry of the current stage). When this occurs, the current counter value is reset to zero and the next stage will become active. If a watchdog timer is fed by software, the timer will return to stage 0 and reset its counter value to zero. Software can feed a watchdog timer by writing any value to `TIMG_WDTFEED_REG` for MDWTs and `RTC_CNTL_WDT_FEED` for RWDT.

### 12.2.2.2 Stages and Timeout Actions

Timer stages allow for a timer to have a series of different timeout values and corresponding expiry action. When one stage expires, the expiry action is triggered, the counter value is reset to zero, and the next stage becomes active. MWDTs/ RWDT provide four stages (called stages 0 to 3). The watchdog timers will progress through each stage in a loop (i.e. from stage 0 to 3, then back to stage 0).

Timeout values of each stage for MWDTs are configured in `TIMG_WDTCONFIGi_REG` (where *i* ranges from 2 to 5), whilst timeout values for RWDT are configured using `RTC_CNTL_WDT_STGj_HOLD` field (where *j* ranges from 0 to 3).

Please note that the timeout value of stage 0 for RWDT (`Thold0`) is determined by the combination of the

`EFUSE_WDT_DELAY_SEL` field of eFuse register `EFUSE_RD_REPEAT_DATA1_REG` and
`RTC_CNTL_WDT_STGO_HOLD`. The relationship is as follows:

```math
T_{hold0} = RTC_CNTL_WDT_STG0_HOLD << (EFUSE_WDT_DELAY_SEL + 1)
```

where `<<` is a left-shift operator.

Upon the expiry of each stage, one of the following expiry actions will be executed:

* Trigger an interrupt

    When the stage expires, an interrupt is triggered.

* CPU reset – Reset a CPU core

    When the stage expires, the CPU core will be reset.

* Core reset – Reset the main system

    When the stage expires, the main system (which includes MWDTs, CPU, and all peripherals) will be reset. The power management unit and RTC peripheral will not be reset.

* System reset – Reset the main system, power management unit and RTC peripheral

    When the stage expires the main system, power management unit and RTC peripheral (see details in Chapter 9 Low-power Management) will all be reset. This action is only available in RWDT.

* Disabled

    This stage will have no effects on the system.

For MWDTs, the expiry action of all stages is configured in `TIMG_WDTCONFIG0_REG`. Likewise for RWDT, the expiry action is configured in `RTC_CNTL_WDTCONFIG0_REG`.

### 12.2.2.3 Write Protection

Watchdog timers are critical to detecting and handling erroneous system/software behavior, thus should not be disabled easily (e.g. due to a misplaced register write). Therefore, MWDTs and RWDT incorporate a write
```