

```markdown
| Code | Source                     | Reset Type   | Note                                                                 |
|------|----------------------------|--------------|-----------------------------------------------------------------------|
| 0x01 | Chip reset¹                | Chip Reset   | —                                                                     |
| 0x0F | Brown-out system re-set    | Chip Reset or System Reset | Triggered by brown-out detector²                                    |
| 0x10 | RWDT system reset          | System Reset | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x12 | Super Watchdog reset       | System Reset | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x03 | Software system reset      | Core Reset   | Triggered by configuring LP_AON_HPSYS_SW_RESET                       |
| 0x05 | Deep-sleep reset           | Core Reset   | See Chapter 11 Low-Power Management                                  |
| 0x07 | MWDTO core reset           | Core Reset   | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x08 | MWDT1 core reset           | Core Reset   | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x09 | RWDT core reset            | Core Reset   | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x14 | eFuse reset                | Core Reset   | Triggered by eFuse CRC error                                         |
|      |                            |              | Triggered when external USB host sends a specific command to the serial interface of USB Serial/JTAG Controller. See Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG) |
| 0x15 | USB (UART) reset           | Core Reset   |                                                                 |
|      |                            |              | Triggered when external USB host sends a specific command to the JTAG interface of USB Serial/JTAG Controller. See Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG) |
| 0x16 | USB (JTAG) reset           | Core Reset   |                                                                 |
| 0xOB | MWDTO CPU reset            | CPU Reset    | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0xOC | Software CPU reset         | CPU Reset    | Triggered by configuring LP_AON_CPU_COREO_SW_RESET                   |
| 0xOD | RWDT CPU reset             | CPU Reset    | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x11 | MWDT1 CPU reset            | CPU Reset    | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x17 | Voltage glitch reset       | System Reset | Triggered by power supply glitch attack                              |
| 0x18 | JTAG CPU reset             | CPU Reset    | Triggered when a "JDB Resetting CPU" instruction is received         |

---

¹ Chip Reset can be triggered by the following sources:
- Triggered by chip power-up.
- Triggered by brown-out detector.

² Once brown-out status is detected, the detector will trigger System Reset or Chip Reset, depending on the register configuration. See Chapter 11 Low-Power Management.
```

## 7.1.5 Peripheral Reset

Peripherals can be reset individually by configuring corresponding registers, or globally by core reset, system reset, or chip reset. After releasing peripherals from reset, the reset release status registers can be read to determine the reset status. These registers turning to 1 indicates that peripherals have been released from reset and can operate properly.

The reset registers of ESP32-H2 peripherals are controlled by the Power/Clock/Reset (PCR) module. For reset