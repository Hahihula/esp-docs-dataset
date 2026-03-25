

```markdown
|Code|Source|Reset Type|Note|
|:-----|:--------------------------|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|0x16|USB (JTAG) reset|Core Reset|Triggered when external USB host sends a specific command to the JTAG interface of USB Serial/JTAG Controller. See Chapter 37 USB Serial/JTAG Controller|
|0x03|Software system reset|Core Reset|Triggered by configuring LP_AON_HPSYS_SW_RESET|
|0x0D|RWDT CPU reset|CPU Reset|See Chapter 16 Watchdog Timers (WDT)|
|0x0C|Software CPU reset|CPU Reset|Triggered by configuring LP_AON_CPU_COREO_SW_RESET|
|0x0B|MWDTO CPU reset|CPU Reset|See Chapter 16 Watchdog Timers (WDT)|
|0x11|MWDT1 CPU reset|CPU Reset|See Chapter 16 Watchdog Timers (WDT)|
|0x18|JTAG CPU reset|CPU Reset|Triggered when a "JDB Resetting CPU" instruction is received|
|0x05|Deep-sleep reset|Core Reset|See Chapter 13 Low-Power Management|
```