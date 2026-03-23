

```markdown
Chapter 15 Watchdog Timers (WDT)	603Back

15.2 Digital Watchdog Timers

15.2.1 Features

Watchdog timers have the following features:

* Four stages, each with a separately programmable timeout value and timeout action
* Timeout actions:
    - MWDT: interrupt, CPU reset, core reset
    - RWDT: interrupt, CPU reset, core reset, system reset
* Flash boot protection at stage 0:
    - MWDTO: core reset upon timeout
    - RWDT: system reset upon timeout
* Write protection that makes WDT register read only unless unlocked
* 32-bit timeout counter
* Clock source:
    - MWDT: PLL_F8OM_CLK, RC_FAST_CLK or XTAL_CLK
    - RWDT: RTC_SLOW_CLK
```