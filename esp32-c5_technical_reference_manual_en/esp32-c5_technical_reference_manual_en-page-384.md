

```markdown
| Code | Source                     | Reset Type   | Note                                                                 |
|------|----------------------------|--------------|-----------------------------------------------------------------------|
| 0x1A | CPU lockup reset           | CPU Reset    | —                                                                     |
| 0x01 | Chip reset¹                | Chip Reset   | —                                                                     |
| 0x12 | Super watchdog reset       | System Reset | See Chapter 16 Watchdog Timers (WDT)                                 |
| 0x19 | Power glitch reset         | System Reset | See Chapter 21 Power Supply Detector                                |
| 0xOF | Brown-out system re- or System reset | Chip Reset<br>System Reset | Triggered by brown-out detector²                                    |
| 0x10 | RWDT system reset          | System Reset | See Chapter 16 Watchdog Timers (WDT)                                 |
| 0x09 | RWDT core reset            | Core Reset   | See Chapter 16 Watchdog Timers (WDT)                                 |
| 0x14 | eFuse reset                | Core Reset   | Triggered by eFuse CRC error check                                   |
| 0x07 | MWDTO core reset           | Core Reset   | See Chapter 16 Watchdog Timers (WDT)                                 |
| 0x08 | MWDT1 core reset           | Core Reset   | See Chapter 16 Watchdog Timers (WDT)                                 |
| 0x15 | USB (UART) reset           | Core Reset   | Triggered when external USB host sends a specific command to the serial interface of USB Serial/JTAG Controller. See Chapter 37 USB Serial/JTAG Controller |

Cont’d on next page
```