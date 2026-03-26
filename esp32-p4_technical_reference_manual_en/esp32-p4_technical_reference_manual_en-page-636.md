

```markdown
|Code|Source|Reset Type|Note|
|:-----|:-----------------------------|:-------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|0xOF|Brown-out system re-set|Chip Reset or System Reset|Triggered by the brown-out detector. Once brown-out status is detected, the detector will trigger System Reset or Chip Reset, depending on the register configuration. See Chapter 14 Low-Power Management|
|0x10|RWDT system reset|System Reset|See Chapter 17 Watchdog Timers (WDT)|
|0x12|Super Watchdog reset|System Reset|See Chapter 17 Watchdog Timers (WDT)|
|0x13|Power glitch reset|System Reset|See Chapter 23 Brown-out Detector|
|0x1B|PSDET reset|System Reset|See Chapter 24 Power Supply Detector (PSDET)|
|0x14|eFuse reset|HP Core Reset|Triggered by eFuse CRC error|
|0x16|USB (JTAG) reset|HP Core Reset|Triggered when external USB host sends a specific command to the JTAG interface of USB Serial/JTAG Controller. See Chapter 51 USB Serial/JTAG Controller (USB_SERIAL_JTAG)|
|0x17|USB (UART) reset|HP Core Reset|Triggered when external USB host sends a specific command to the serial interface of USB Serial/JTAG Controller. See Chapter 51 USB Serial/JTAG Controller (USB_SERIAL_JTAG)|
|0x18|JTAG CPU reset|HP CPUO/1 Reset|Triggered when a “GDB Resetting CPU” instruction is received|
|0x1A|Lockup reset|HP CPUO/1 Reset|Triggered when the CPU enters lockup. HP CPUO and HP CPU1 can be reset in lockup state by configuring LP_CLKRST_HPCOREx_LOCKUP_RESET_EN|

- Chip Reset can be triggered by the following sources:
  - Chip power-up
  - Brown-out detector

- The HP system contains two watchdog timers called Main System Watchdog Timers (MWDT), and the MWDT that can trigger reset can be configured via `HP_SYS_CLKRST_HPCOREO_WDT_RESET_SOURCE_SEL` and `HP_SYS_CLKRST_HPCOREO_WDT_RESET_SOURCE_SEL` for HP CPUO and HP CPU1 respectively.

Table 10.1-2. LP CPU Reset Source
```