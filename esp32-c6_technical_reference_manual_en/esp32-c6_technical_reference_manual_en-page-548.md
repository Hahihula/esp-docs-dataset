

```markdown
15.2.2 Functional Description

Figure 15.2-1 shows the three watchdog timers in ESP32-C6 digital systems.

15.2.2.1 Clock Source and 32-Bit Counter

At the core of each watchdog timer is a 32-bit counter.

Take MWDTO as an example:

*   MWDTO can select between the PLL_F80M_CLK, RC_FAST_CLK or XTAL_CLK (external) clock as its clock source by setting the PCR_TGO_WDT_CLK_SEL field of the PCR_TIMERGROUP0_WDT_CLK_CONF_REG register.
*   The selected clock is switched on by setting PCR_TGO_WDT_CLK_EN field of the PCR_TIMERGROUP0_WDT_CLK_CONF_REG register to 1 and switched off by setting it to 0. Then the selected clock is divided by a 16-bit configurable prescaler. See more details in Table 8.2-1 of Chapter 8.

The 16-bit prescaler for MWDT is configured via the TIMG_WDT_CLK_PRESCALE field of TIMG_WDTOCONFIG1_REG. When TIMG_WDT_DIVCNT_RST field is set, the prescaler is reset and it can be re-configured at once.

In contrast, the clock source of RWDT is derived directly from RTC_SLOW_CLK (see details in Chapter 8 Reset and Clock).
```