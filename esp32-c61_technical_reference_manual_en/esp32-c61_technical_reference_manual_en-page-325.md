

```markdown
| Code | Source                     | Reset Type   | Note                                                                 |
|------|-----------------------------|--------------|-----------------------------------------------------------------------|
| 0x16 | USB (JTAG) reset            | Core Reset   | Triggered when external USB host sends a specific command to the JTAG interface of USB Serial/JTAG Controller. See Chapter 29 USB Serial/JTAG Controller |
| 0x03 | Software system reset       | Core Reset   | Triggered by configuring LP_AON_HPSYS_SW_RESET                       |
| 0x0D | RWDT CPU reset              | CPU Reset    | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x0C | Software CPU reset          | CPU Reset    | Triggered by configuring LP_AON_CPU_COREO_SW_RESET                   |
| 0x0B | MWDTO CPU reset             | CPU Reset    | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x11 | MWDT1 CPU reset             | CPU Reset    | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x18 | JTAG CPU reset              | CPU Reset    | Triggered when a "JDB Resetting CPU" instruction is received         |
| 0x1A | CPU lockup reset            | CPU Reset    | Triggered when CPU lockup                                           |
| 0x05 | Deep-sleep reset            | Core Reset   | See Chapter 11 Low-Power Management                                  |

```

7.1.5 Peripheral Reset

Peripherals can be reset individually by configuring corresponding registers, or globally by core reset, system reset, or chip reset. After releasing peripherals from reset, the reset release status registers can be read to determine the reset status. These registers turning to 1 indicates that peripherals have been released from reset and can operate properly.

The reset registers of ESP32-C61’s HP system peripherals are controlled by the Power/Clock/Reset (PCR) module. Please see 7.4.1 PCR Register Summary for the reset registers of HP system peripherals and 7.4.2 LP System Clock Register Summary for the clock registers of low-power system peripherals.

7.2 Clock

7.2.1 Overview

ESP32-C61 clocks are mainly sourced from oscillator (OSC), RC, and PLL circuits, and then processed by the dividers or selectors, which allows most functional modules to select their working clock according to their power consumption and performance requirements. Figure 7.2-1 shows the system clock structure.
```