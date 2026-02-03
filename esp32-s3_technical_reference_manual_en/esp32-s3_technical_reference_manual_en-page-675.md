**Chapter Title:**
Chapter 13 Watchdog Timers (WDT)

**Section Header:**
13.2.2 Functional Description

**Diagram and Figure Caption:**
- Diagram showing the clock source for watchdog timers in ESP32-S3 digital systems.
- **Figure 13.2-1:** Clock Source and 32-Bit Counter
- The diagram includes components such as TIMG0, TIMG1 (Timer Group), Prescaler, APB_CLK, RTC, RWDT, with various configuration registers like TIMGO_WDT_EN, TIMGO_WDT.Feedback, TIMGO_WDT_WKEY.

**Subsection Title:**
13.2.2.1 Clock Source and 32-Bit Counter

**Body Text:**
At the core of each watchdog timer is a 32-bit counter. The clock source of MWDTs is derived from the APB clock via a pre-MWDT 16-bit configurable prescaler. In contrast, the clock source of RWDT is derived directly from an RTC slow clock (the RTC slow clock source shown in Chapter 7 Reset and Clock). The 16-bit prescaler for MWDTs is configured via the TIMG_WDT_CLK_PRESCALE field of TIMG_WDTCONFIG1_REG.

MWDTs and RWDT are enabled by setting the TIMG_WDT_EN and RTC_CNTL_WDT_EN fields respectively. When enabled, the 32-bit counters of each watchdog will increment on each source clock cycle until the timeout value of the current stage is reached (i.e., expiry of the current stage). When this occurs, the current counter value is reset to zero and the next stage will become active.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)