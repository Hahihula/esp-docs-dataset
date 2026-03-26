

```markdown
Chapter 17 Watchdog Timers (WDT) GoBack

Note that while this chapter provides the functional descriptions of the watchdog timer's, MWDT register descriptions are detailed in Chapter 16 Timer Group (TIMG), and the RWDT and SWD register descriptions are detailed in Section 17.5 Register Summary.

## 17.2 Digital Watchdog Timers

### 17.2.1 Features

Watchdog timers have the following features:

* Four stages, each with a separately programmable timeout value and timeout action
* Timeout actions:
    * MWDT: interrupt, HP CPU reset, HP core reset
    * RWDT: interrupt, HP CPU reset, HP core reset, system reset
* Flash boot protection under SPI Boot mode at stage 0:
    * MWDTO: HP core reset upon timeout
    * RWDT: system reset upon timeout
* Write protection that makes WDT register read only unless unlocked
* 32-bit timeout counter
* Clock source:
    * MWDT: PLL_F8OM_CLK, RC_FAST_CLK or XTAL_CLK
    * RWDT: LP_DYN_SLOW_CLK
```