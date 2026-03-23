

```markdown
Note that while this chapter provides the functional descriptions of the watchdog timer's, their register descriptions are provided in Chapter 11 Timer Group (TIMG) and Chapter 9 Low-power Management.

## 12.2 Digital Watchdog Timers

### 12.2.1 Features

Watchdog timers have the following features:

* Four stages, each with a programmable timeout value. Each stage can be configured and enabled/disabled separately
* Three timeout actions (interrupt, CPU reset, or core reset) for MWDT and four timeout actions (interrupt, CPU reset, core reset, or system reset) for RWDT upon expiry of each stage
* 32-bit expiry counter
* Write protection, to prevent RWDT and MWDT configuration from being altered inadvertently
* Flash boot protection

If the boot process from an SPI flash does not complete within a predetermined period of time, the watchdog will reboot the entire main system.
```