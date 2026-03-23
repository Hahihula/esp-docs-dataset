

```markdown
## 12.2.2 Functional Description

Figure 12.2-1 shows the three watchdog timers in ESP32-C3 digital systems.

### 12.2.2.1 Clock Source and 32-Bit Counter

At the core of each watchdog timer is a 32-bit counter.

MWDTs can select between the APB clock (APB_CLK) or external clock (XTAL_CLK) as its clock source by setting the TIMG_WDT_USE_XTAL field of the TIMG_WDTCONFIG0_REG register. The selected clock is switched on by setting TIMG_WDT_CLK_IS_ACTIVE field of the TIMG_REGCLK_REG register to 1 and switched off by setting it to 0. Then the selected clock is divided by a 16-bit configurable prescaler. The 16-bit prescaler for MWDTs is configured via the TIMG_WDT_CLK_PRESCALE field of TIMG_WDTCONFIG1_REG.When TIMG_WDT_DIVCNT_RST field is set, the prescaler is reset and it can be re-configured at once.

In contrast, the clock source of RWDT is derived directly from an RTC slow clock (the RTC slow clock source shown in Chapter 6 Reset and Clock).

MWDTs and RWDT are enabled by setting the TIMG_WDT_EN and RTC_CNTL_WDT_EN fields respectively.
```

Figure 12.2-1 Watchdog Timers in ESP32-C3

```plaintext
DIGITAL

APB_CLK ──┐
          │
          ├─ Prescaler (16 bits) ──► mwdt0 clk
          │
          └─ TIMG0_WDTCONFIG1_REG
             TIMG0_WDT_CLK_PRESCALE
             TIMG0_WDT_DIVCNT_RST

Timer Group 0
┌──────────────────────┐
│                     │
│ TIMG0_WDT_EN        │
│ TIMG0_WDTFEED_REG   │
│ TIMG0_WDT_WKEY      │
└──────────────────────┘
          │
          ├─ TIMG0_WDT_CPU_RESET
          ├─ TIMG0_WDT_CORE_RESET
          └─ TIMG0_WDT_INT

APB_CLK ──┐
          │
          ├─ Prescaler (16 bits) ──► mwdt1 clk
          │
          └─ TIMG1_WDTCONFIG1_REG
             TIMG1_WDT_CLK_PRESCALE
             TIMG1_WDT_DIVCNT_RST

Timer Group 1
┌──────────────────────┐
│                     │
│ TIMG1_WDT_EN        │
│ TIMG1_WDTFEED_REG   │
│ TIMG1_WDT_WKEY      │
└──────────────────────┘
          │
          ├─ TIMG1_WDT_CPU_RESET
          ├─ TIMG1_WDT_CORE_RESET
          └─ TIMG1_WDT_INT

RTC
┌──────────────────────┐
│                     │
│ RTC_CNTL_WDT_EN     │
│ RTC_CNTL_WDT_FEED   │
│ RTC_CNTL_WDT_WKEY   │
└──────────────────────┘
          │
          ├─ RTC_SLOW_CLK ──►
          │
          └─ RWDT

Outputs:
TIMG0_WDT_EN, TIMG1_WDT_EN, RTC_CNTL_WDT_EN → enable signals for respective timers.
```

Figure 12.2-1 Watchdog Timers in ESP32-C3 digital systems.

```markdown
Espressif Systems    307        ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback
```