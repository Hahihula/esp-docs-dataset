
Chapter 7 Reset and Clock

- CPU Reset: resets CPU core. Once such a reset is released, the instructions from the CPU reset vector (0x40000000) will be executed.
- Core Reset: resets the whole digital system except LP system, including CPU, peripherals, digital GPIOs, Wireless MAC and Baseband.
- System Reset: resets the whole digital system, including LP system.
- Chip Reset: resets the whole chip, including the digital system and analog system.

• Software reset and hardware reset:
  - Software Reset: triggered via software by configuring the corresponding registers of CPU, see Chapter 11 Low-Power Management.
  - Hardware Reset: triggered directly by the hardware.

7.1.4 Functional Description

CPU will be reset immediately when any type of reset above occurs. Users can retrieve reset source codes by reading LP_CLKRST_RESET_CAUSE after the reset is released. The current reset source recorded in the LP_CLKRST_RESET_CAUSE register can be cleared by configuring LP_CLKRST_COREO_RESET_CAUSE_CLR.

Table 7.1-1 lists possible reset sources and the types of reset they trigger. When multiple reset sources are active simultaneously, the reset source recorded in LP_CLKRST_RESET_CAUSE is the most top one among the active reset sources listed in Table 7.1-1. When multiple reset sources are active but not at the same time, LP_CLKRST_RESET_CAUSE records the most recent reset source.

Table 7.1-1. Reset Source

| Code | Source                     | Reset Type         | Note                                                                 |
|------|----------------------------|--------------------|-----------------------------------------------------------------------|
| 0x01 | Chip reset¹                | Chip Reset         | —                                                                     |
| 0x12 | Super watchdog reset       | System Reset       | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x19 | Power glitch reset         | System Reset       | See Chapter 19 Power Supply Detector                                |
| 0x0F | Brown-out system re-set    | Chip Reset or System Reset | Triggered by brown-out detector²                               |
| 0x10 | RWDT system reset           | System Reset       | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x09 | RWDT core reset             | Core Reset         | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x14 | eFuse reset                 | Core Reset         | Triggered by eFuse CRC error check                                   |
| 0x07 | MWDTO core reset            | Core Reset         | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x08 | MWDT1 core reset            | Core Reset         | See Chapter 14 Watchdog Timers (WDT)                                 |
| 0x15 | USB (UART) reset            | Core Reset         | Triggered when external USB host sends a specific command to the serial interface of USB Serial/JTAG Controller. See Chapter 29 USB Serial/JTAG Controller |

Cont'd on next page

Espressif Systems
324
ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback
PRELIMINARY