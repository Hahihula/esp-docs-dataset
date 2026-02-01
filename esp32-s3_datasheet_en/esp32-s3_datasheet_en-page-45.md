**4 Functional Description**

---

### **4.1.3.6 System Timer**

ESP32-S3 integrates a 52-bit system timer, which has two 52-bit counters and three comparators.

#### Feature List

- Counters with a clock frequency of 16 MHz
- Three types of independent interrupts generated according to alarm value
- Two alarm modes: target mode and period mode
- 52-bit target alarm value and 26-bit periodic alarm value
- Read sleep time from RTC timer when the chip is awakened from Deep-sleep or Light-sleep mode
- Counters can be stalled if the CPU is stalled or in OCD mode

For details, see [ESP32-S3 Technical Reference Manual > Chapter System Timer](#).

---

### **4.1.3.7 General Purpose Timers**

ESP32-S3 is embedded with four 54-bit general-purpose timers, which are based on 16-bit prescalers and 54-bit auto-reload-capable up/down-timers.

#### Feature List

- 16-bit clock prescaler, from 2 to 65536
- 54-bit time-base counter programmable to be incrementing or decrementing
- Able to read real-time value of the time-base counter
- Halting and resuming the time-base counter
- Programmable alarm generation
- Timer value reload (Auto-reload at alarm or software-controlled instant reload)
- Level interrupt generation

For details, see [ESP32-S3 Technical Reference Manual > Chapter Timer Group](#).

---

### **4.1.3.8 Watchdog Timers**

ESP32-S3 contains three watchdog timers: one in each of the two timer groups (called Main System Watchdog Timers, or MWDT) and one in the RTC Module (called the RTC Watchdog Timer, or RWDT). During the flash boot process, RWDT and the first MWDT are enabled automatically in order to detect and recover from booting errors.

#### Feature List

- Four stages:
  - Each with a programmable timeout value
  - Each stage can be configured, enabled and disabled separately

---

**Espressif Systems**

45 [Submit Documentation Feedback](#) ESP32-S3 Series Datasheet v2.1