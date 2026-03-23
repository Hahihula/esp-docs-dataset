
```markdown
| Code | Source                     | Reset Type         | Comments                                                                                      |
|------|----------------------------|--------------------|-----------------------------------------------------------------------------------------------|
| 0x01 | Chip reset¹                | Chip Reset         | -                                                                                             |
| 0x0F | Brown-out system reset     | Chip Reset or System Reset | Triggered by brown-out detector²                                                            |
| 0x10 | RWDT system reset          | System Reset       | See Chapter 12 Watchdog Timers (WDT)                                                         |
| 0x12 | Super Watchdog reset       | System Reset       | See Chapter 12 Watchdog Timers (WDT)                                                         |
| 0x13 | CLK GLITCH reset           | System Reset       | See Chapter 25 Clock Glitch Detection                                                       |
| 0x03 | Software system reset      | Core Reset         | Triggered by configuring RTC_CNTL_SW_SYS_RST                                                 |
| 0x05 | Deep-sleep reset           | Core Reset         | See Chapter 9 Low-power Management                                                          |
| 0x07 | MWDTO core reset           | Core Reset         | See Chapter 12 Watchdog Timers (WDT)                                                         |
| 0x08 | MWDT1 core reset           | Core Reset         | See Chapter 12 Watchdog Timers (WDT)                                                         |
| 0x09 | RWDT core reset            | Core Reset         | See Chapter 12 Watchdog Timers (WDT)                                                         |
| 0x14 | eFuse reset                | Core Reset         | Triggered by eFuse CRC error                                                                 |
|      |                            |                    | Triggered when external USB host sends a specific command to the Serial interface of USB-Serial-JTAG. See 30 USB Serial/JTAG Controller (USB_SERIAL_JTAG) |
| 0x15 | USB (UART) reset           | Core Reset         | Triggered when external USB host sends a specific command to the JTAG interface of USB-Serial-JTAG. See 30 USB Serial/JTAG Controller (USB_SERIAL_JTAG) |
| 0x16 | USB (JTAG) reset           | Core Reset         |                                                                                               |
| 0x17 | Power glitch reset         | Core Reset         | Triggered by power glitch                                                                     |
| 0x0B | MWDTO CPU reset            | CPU Reset          | See Chapter 12 Watchdog Timers (WDT)                                                         |
| 0x0C | Software CPU reset         | CPU Reset          | Triggered by configuring RTC_CNTL_SW_PROCPU_RST                                               |
| 0x0D | RWDT CPU reset             | CPU Reset          | See Chapter 12 Watchdog Timers (WDT)                                                         |
| 0x11 | MWDT1 CPU reset            | CPU Reset          | See Chapter 12 Watchdog Timers (WDT)                                                         |

¹ Chip Reset can be triggered by the following two sources:
- Triggered by chip power-on.
- Triggered by brown-out detector.

² Once brown-out status is detected, the detector will trigger System Reset or Chip Reset, depending on register configuration. See Chapter 9 Low-power Management.
```

## 6.2 Clock

### 6.2.1 Overview

ESP32-C3 clocks are mainly sourced from oscillator (OSC), RC, and PLL circuit, and then processed by the dividers or selectors, which allows most functional modules to select their working clock according to their power consumption and performance requirements. Figure 6.2-1 shows the system clock structure.
```