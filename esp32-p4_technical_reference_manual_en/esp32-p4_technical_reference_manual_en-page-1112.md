

```markdown
DIGITAL

MWDTO clock Selection & gating                    TIMG0_WDTCONFIG1_REG
TIMG0_WDT_CLK_PRESCALE                          TIMG0_WDT_EN
TIMG0_WDT_DIVCNT_RST                            TIMG0_WDTFEED_REG
                                               TIMG0_WDT_WKEY

Prescaler (16 bits)                              mwdt0 clk

MWDTO

TIMG0_WDT_CPU_RESET Signal
TIMG0_WDT_CORE_RESET Signal
TIMG0_WDT_INT Signal

Timer Group 0

MWDT1 clock Selection & gating                   TIMG1_WDTCONFIG1_REG
TIMG1_WDT_CLK_PRESCALE                          TIMG1_WDT_EN
TIMG1_WDT_DIVCNT_RST                            TIMG1_WDTFEED_REG
                                               TIMG1_WDT_WKEY

Prescaler (16 bits)                              mwdt1 clk

MWDT1

TIMG1_WDT_CPU_RESET Signal
TIMG1_WDT_CORE_RESET Signal
TIMG1_WDT_INT Signal

Timer Group 1

RTC

LP_DYN_SLOW_CLK                                  RTC_WDT_EN
                                               RTC_WDT_FEED
                                               RTC_WDT_WKEY

RWDT

RTC_WDT_CPU_RESET Signal
RTC_WDT_SYS_RESET Signal
RTC_WDT_CORE_RESET Signal
RTC_WDT_INT Signal

Figure 17.2-1. Digital Watchdog Timers in ESP32-P4

Figure 17.2-1 shows the three watchdog timers in ESP32-P4 digital systems.

17.2.2.1 Clock Source and 32-Bit Counter

At the core of each watchdog timer is a 32-bit counter.

Take MWDTO as an example:

*   MWDTO can select between the PLL_F80M_CLK, RC_FAST_CLK or XTAL_CLK (external) clock as its clock source by setting the HP_SYS_TIMERGRPO_WDT_SRC_SEL field of the HP_SYS_CLKRST_PERI_CLK_CTRL20_REG register.
*   The selected clock is switched on by setting HP_SYS_TIMERGRPO_WDT_CLK_EN field of the HP_SYS_CLKRST_PERI_CLK_CTRL20_REG register to 1 and switched off by setting it to 0. Then the selected clock is divided by a 16-bit configurable prescaler. See more details in Table 10.2-1 of Chapter 10.
*   The 16-bit prescaler for MWDT is configured via the TIMG_WDT_CLK_PRESCALE field of TIMG_WDTCONFIG1_REG. When TIMG_WDT_DIVCNT_RST field is set, the prescaler is reset and it can be re-configured at once.
```