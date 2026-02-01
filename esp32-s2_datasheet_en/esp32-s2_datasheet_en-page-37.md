Title: Functional Description

- halting and resuming the time-base counter
- programmable alarm generation
- timer value reload (Auto-reload at alarm or software-controlled instant reload)
- level and edge interrupt generation

For more information, please refer to [ESP32-S2 Technical Reference Manual > Chapter Timer Group (TIMG)](#).

Subtitle: Watchdog Timers

Body Text:
The ESP32-S2 contains three watchdog timers: one in each of the two timer groups (called Main System Watchdog Timers, or MWDT) and one in the RTC Module (called the RTC Watchdog Timer, or RWDT). Each watchdog timer allows for four separately configurable stages and each stage can be programmed to take one of three (or four for RWDT) actions upon expiry, unless the watchdog is fed or disabled. The actions upon expiry are: interrupt, CPU reset, core reset and system reset. Only RWDT can trigger a system reset that will reset the entire digital circuits, which is the main system including the RTC itself. A timeout value can be set for each stage individually.

During the flash boot process, RWDT and the first MWDT are enabled automatically in order to detect and recover from booting errors.

Subtitle: Watchdog timers have the following features:

- four stages, each with a programmable timeout value. Each stage can be configured and enabled/disabled separately
- one of three/four (for MWDTs/ RWDT) possible actions (interrupt, CPU reset, core reset and system reset) available upon expiry of each stage
- 32-bit expiry counter
- write protection, to prevent RWDT and MWDT configuration from being altered inadvertently
- flash boot protection

If the boot process from an SPI flash does not complete within a predetermined period of time, the watchdog will reboot the entire main system.

For more information, please refer to [ESP32-S2 Technical Reference Manual > Chapter Watchdog Timers (WDT)](#).

Title: 4.1.3.3 Power Management Unit

Body Text:
With the use of advanced power-management technologies, ESP32-S2 can switch between different power modes.

- Active mode: CPU and chip radio are powered on. The chip can receive, transmit, or listen.
- Modem-sleep mode: The CPU is operational and the clock speed can be reduced. The Wi-Fi baseband and radio are disabled, but Wi-Fi connection can remain active.
- Light-sleep mode: The CPU is paused. The RTC peripherals, as well as the ULP co-processor are running. Any wake-up events (MAC, RTC timer, or external interrupts) will wake up the chip. Wi-Fi connection can remain active.

Footer:
Espressif Systems
37
[Submit Documentation Feedback](#)
ESP32-S2 Series Datasheet v1.8