**Title: Functional Description**

---

### 4.1.3.7 Timer Group

ESP32-C3 has two 54-bit general-purpose timers, which are based on 16-bit prescalers and 54-bit auto-reload-capable up/down timers.

The timers’ features are summarized as follows:
- a **16-bit clock prescaler**, from 1 to 65536
- a **54-bit time-base counter** programmable to be incrementing or decrementing
- able to read real-time value of the time-base counter
- halting and resuming the time-base counter
- programmable alarm generation
- level interrupt generation

For details, see [ESP32-C3 Technical Reference Manual > Chapter Timer Group (TIMG)](#).

---

### 4.1.3.8 Watchdog Timers

For details, see [ESP32-C3 Technical Reference Manual > Chapter Watchdog Timers](#).

#### Digital Watchdog Timers

ESP32-C3 contains three digital watchdog timers: one in each of the two timer groups (called Main System Watchdog Timers, or MWDT) and one in the RTC module (called the RTC Watchdog Timer, or RWDT).

During the flash boot process, RWDT and the MWDT in timer group 0 (TIMGO) are enabled automatically in order to detect and recover from booting errors.

Digital watchdog timers have the following features:
- four stages, each with a programmable timeout value. Each stage can be configured, enabled and disabled separately
- interrupt, CPU reset, or core reset for MWDT upon expiry of each stage; interrupt, CPU reset, core reset, or system reset for RWDT upon expiry of each stage
- 32-bit expiry counter
- write protection, to prevent RWDT and MWDT configuration from being altered inadvertently
- flash boot protection

If the boot process from an SPI flash does not complete within a predetermined period of time, the watchdog will reboot the entire main system.

#### Analog Watchdog Timer

ESP32-C3 also has one analog watchdog timer: RTC super watchdog timer (SWD). It is an ultra-low-power circuit in analog domain that helps to prevent the system from operating in a sub-optimal state and resets the system if required.

SWD has the following features:
- Ultra-low power
- Low standby current

---

**Footer:**  
Espressif Systems  
40  
[Submit Documentation Feedback](#)  
ESP32-C3 Series Datasheet v2.2