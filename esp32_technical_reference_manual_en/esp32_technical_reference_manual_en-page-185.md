**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Body Text:**

- **RTC main state machine:** records the power state.
  
- **Digital & analog power controller:** generates actual power-gating/clock gating signals for digital parts and analog parts.

- **Sleep & wakeup controller:** handles the entry into & exit from the low-power mode.

- **Timers:** include RTC main timer, ULP coprocessor timer and touch timer.

- **Low-Power processor and sensor controllers:** include ULP coprocessor, touch controller, SAR ADC controller, etc.

- **Retention memory:**
  - RTC slow memory: an 8 KB SRAM, mostly used as retention memory or instruction & data memory for the ULP coprocessor. The CPU accesses it through the APB, starting from address 0x50000000.
  - RTC fast memory: an 8 KB SRAM, mostly used as retention memory. The CPU accesses it through IRAMO/DRAMO. Fast RTC memory is about 10 times faster than the RTC slow memory.

- **Retention registers:** always-on registers of 8 x 32 bits, serving as data storage.
  
- **RTC IO pads:** 18 always-on analog pads, usually functioning as wake-up sources.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback