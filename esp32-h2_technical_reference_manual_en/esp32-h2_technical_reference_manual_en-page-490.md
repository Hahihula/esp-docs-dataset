

```markdown
DIGITAL

MWDT0 clock
Selection & gating → Prescaler (16 bits) → mwdt0 clk → MWDT0
Timer Group 0

MWDT1 clock
Selection & gating → Prescaler (16 bits) → mwdt1 clk → MWDT1
Timer Group 1

RTC SLOW_CLK → RWDT → CPU reset
                              System reset
                              Core reset
                              Interrupt

Figure 14.2-1. Digital Watchdog Timers in ESP32-H2
```

### 14.2.2 Functional Description

#### 14.2.2.1 Clock Source and 32-Bit Counter

At the core of each watchdog timer is a 32-bit counter.

Take MWDTO in Timer Group 0 as an example:

- MWDTO can select between the PLL_F48M_CLK, RC_FAST_CLK or XTAL_CLK (external) clock as its clock source by setting the `PCR_TGO_WDT_CLK_SEL` field of the `PCR_TIMERGROUP0_WDT_CLK_CONF_REG` register.
- The selected clock is switched on by setting `PCR_TGO_WDT_CLK_EN` field of the `PCR_TIMERGROUP0_WDT_CLK_CONF_REG` register to 1 and switched off by setting it to 0. Then the selected clock is divided by a 16-bit configurable prescaler. See more details in Table 7.2-1 CPU_CLK Clock Source of Chapter 7 Reset and Clock.
- The 16-bit prescaler for MWDTO is configured via the `TIMGn_WDT_CLK_PRESCALE` (n: 0 ~ 1, where for Timer Group 0, the value of n should be 0 here) field of `TIMGn_WDTCONFIG1_REG`. When `TIMGn_WDT_DIVCNT_RST` field is set, the prescaler is reset and it can be re-configured at once.

In contrast, the clock source of RWDT is derived directly from RTC_SLOW_CLK (see details in Chapter 7 Reset and Clock).
```