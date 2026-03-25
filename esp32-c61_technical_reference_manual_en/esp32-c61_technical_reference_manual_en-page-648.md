

```markdown
14.2.2.3 Write Protection

Watchdog timers are critical to detecting and handling erroneous system/software behavior, and thus should not be disabled easily (e.g. due to a misplaced register write). Therefore, MWDT and RWDT incorporate a write protection mechanism that prevents the watchdogs from being disabled or tampered with due to an accidental write.

The write protection mechanism is implemented using a write-key field for each timer (TIMG_WDT_WKEY for MWDT, RTC_WDT_WKEY for RWDT). The value 0x50D83AA1 must be written to the watchdog timer’s write-key field before any other register of the same watchdog timer can be changed. Any attempts to write to a watchdog timer’s registers (other than the write-key field itself) whilst the write-key field’s value is not 0x50D83AA1 will be ignored. The recommended procedure for accessing a watchdog timer is as follows:

1. Disable the write protection by writing the value 0x50D83AA1 to the timer’s write-key field.
2. Make the required modification of the watchdog such as feeding or changing its configuration.
3. Re-enable write protection by writing any value other than 0x50D83AA1 to the timer’s write-key field.

14.2.2.4 Flash Boot Protection

During flash booting process, MWDTO as well as RWDT, are automatically enabled. Stage 0 for the enabled MWDTO is automatically configured as core reset action upon timeout, known as core reset. Likewise, stage 0 for RWDT is configured to system reset, which resets the main system and RTC when it times out. After booting, TIMG_WDT_FLASHBOOT_MOD_EN and RTC_WDT_FLASHBOOT_MOD_EN should be cleared to stop the flash boot protection procedure for both MWDTO and RWDT respectively. After this, MWDTO and RWDT can be configured by software.

14.3 Super Watchdog

Super watchdog (SWD) is an ultra-low-power circuit in analog domain that helps to prevent the system from operating in a sub-optimal state and resets the system (system reset) if required. SWD contains a watchdog circuit that needs to be fed for at least once during its timeout period, which is slightly less than one second. About 100 ms before watchdog timeout, it will also send out a WD_INTR signal as a request to remind the system to feed the watchdog.

If the system doesn’t respond to SWD feed request and watchdog finally times out, SWD will generate a system level signal SWD_RSTB to reset whole digital circuits on the chip (system reset).

The source of the clock for SWD is constant and can not be selected.

14.3.1 Features

SWD has the following features:

- An analog watchdog that operates independently of the digital circuit and can function in environments where the digital circuit’s clock and voltage are abnormal
- Interrupt to indicate that the SWD is about to time out
```