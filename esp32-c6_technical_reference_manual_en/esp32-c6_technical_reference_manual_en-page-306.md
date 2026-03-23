
```markdown
| Code | Source                     | Reset Type   | Note                                                                 |
|------|----------------------------|--------------|-----------------------------------------------------------------------|
| 0x01 | Chip reset¹                | Chip Reset   | —                                                                     |
| 0x0F | Brown-out system re- set    | Chip Reset or System Reset | Triggered by brown-out detector²                                    |
| 0x10 | RWDT system reset           | System Reset | See Chapter 15 Watchdog Timers (WDT)                                 |
| 0x12 | Super Watchdog reset        | System Reset | See Chapter 15 Watchdog Timers (WDT)                                 |
| 0x03 | Software system reset       | Core Reset   | Triggered by configuring LP_AON_HPSYS_SW_RESET                       |
| 0x05 | Deep-sleep reset            | Core Reset   | See Chapter 12 Low-Power Management                                  |
| 0x06 | SDIO core reset             | Core Reset   | Reserved                                                              |
| 0x07 | MWDTO core reset            | Core Reset   | See Chapter 15 Watchdog Timers (WDT)                                 |
| 0x08 | MWDT1 core reset            | Core Reset   | See Chapter 15 Watchdog Timers (WDT)                                 |
| 0x09 | RWDT core reset             | Core Reset   | See Chapter 15 Watchdog Timers (WDT)                                 |
| 0x14 | eFuse reset                 | Core Reset   | Triggered by eFuse CRC error                                         |
| 0x15 | USB (UART) reset            | Core Reset   | Triggered when external USB host sends a specific command to the Serial interface of USB Serial/JTAG Controller. See Chapter 32 USB Serial/JTAG Controller (USB_SERIAL_JTAG) |
| 0x16 | USB (JTAG) reset            | Core Reset   | Triggered when external USB host sends a specific command to the JTAG interface of USB Serial/JTAG Controller. See Chapter 32 USB Serial/JTAG Controller (USB_SERIAL_JTAG) |
| 0x0B | MWDTO CPU reset             | CPU Reset    | See Chapter 15 Watchdog Timers (WDT)                                 |
| 0x0C | Software CPU reset          | CPU Reset    | Triggered by configuring LP_AON_CPU_COREO_SW_RESET                   |
| 0x0D | RWDT CPU reset              | CPU Reset    | See Chapter 15 Watchdog Timers (WDT)                                 |
| 0x11 | MWDT1 CPU reset             | CPU Reset    | See Chapter 15 Watchdog Timers (WDT)                                 |
| 0x18 | JTAG CPU reset              | CPU Reset    | Triggered when a "JDB Resetting CPU" instruction is received         |

¹ Chip Reset can be triggered by the following sources:
• Triggered by chip power-on.
• Triggered by brown-out detector.

² Once brown-out status is detected, the detector will trigger System Reset or Chip Reset, depending on register configuration. See Chapter 12 Low-Power Management.
```

## 8.1.5 Peripheral Reset

Peripherals can be reset individually by configuring corresponding registers, or globally by Core Reset, System Reset, or Chip Reset. The reset registers of ESP32-C6 peripherals are merged to Power/Clock/Reset (PCR) module. See Section 8.4 Register Summary for detailed information.

## 8.2 Clock
```