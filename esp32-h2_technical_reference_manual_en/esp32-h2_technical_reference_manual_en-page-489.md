

```markdown
Note that while this chapter provides the functional descriptions of the watchdog timer, MWDT register descriptions are detailed in Chapter 13 Timer Group (TIMG), and the RWDT and SWD register descriptions are detailed in Section 14.5 Register Summary.

Note:
Unless otherwise specified, MWDT in this chapter refers to both MWDTO and MWDT1.
```

## 14.2 Digital Watchdog Timers

### 14.2.1 Features

Watchdog timers have the following features:

* Four stages, each with a separately programmable timeout value and timeout action
* Timeout actions:
    * MWDT: interrupt, CPU reset, core reset
    * RWDT: interrupt, CPU reset, core reset, system reset
* Flash boot protection at stage 0:
    * MWDTO: core reset upon timeout
    * RWDT: system reset upon timeout
* Write protection that makes WDT register read only unless unlocked
* 32-bit timeout counter
* Clock source:
    * MWDT: PLL_F48M_CLK, RC_FAST_CLK or XTAL_CLK
    * RWDT: RTC_SLOW_CLK
```