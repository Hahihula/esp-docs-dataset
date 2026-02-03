**Title: Chapter 13 Watchdog Timers (WDT)**

**Body Text:**
the timer will return to stage 0 and reset its counter value to zero. Software can feed a watchdog timer by writing any value to TIMG_WDTFEED_REG for MDWTS and RTC_CNTL_RWDOT_FEED for RWDT.

**Subtitle: 13.2.2 Stages and Timeout Actions**

Timer stages allow for a timer to have a series of different timeout values and corresponding expiry action.
When one stage expires, the expiry action is triggered; when zero value set to expire, next state becomes active. MWDTS/RWDT provide four states (called stages 0-3). The watchdog timers will progress through each stage in loop from stage 0 back to start.

Timeout values for MDWTS are configured in TIMG_WDTCONFIG_i_REG where i ranges from 2 to 5, whilst timeout values RWDT are configured using RTC_CNTL_WDT_STG_HOLD field (where j ranges from 0-3).

Please note that the timeout value of stage zero WRTD (Hold) is determined by combination EFUSE_WDT_DELAY_SEL eFuse register EFUSE_RDD_REPEAT_DATA1_REG and RTC_CNTL_WDT_STG_HOLD. The relationship as follows:

\[ T_{hold} = RTW_CNTL_WDT_STG0_HOLD << (EFUSE_WDT_DELAY_SEL + 1) \]

where << is a left-shift operator.

Upon expiry of each stage, one the following expiry actions will be executed:
- Trigger an interrupt
- CPU reset – Reset core when expires; the CPU core will be reset.
- Core reset - Reset main system When expire: the main (which includes MDWTS, CPU and all peripherals) will be reset. The power management unit RTC peripheral not set.

- System reset – Reset entire chip including power managements units RTC peripheral
When stage expires when main; power management unit RTC peripheral

**Subtitle: 13.2.3 Write Protection**

Watchdog timers critical to detecting handling erroneous system/software behavior, thus should be disabled easily (e.g., due misplaced register write). Therefore MWDTS RWDT incorporate a protection mechanism that prevent watchdogs from being disabled tampered accidental writes.

**Footer:**  
Espressif Systems  
676 ESP32-S3 TRM (Version 1.7)  

**Link:** Submit Documentation Feedback