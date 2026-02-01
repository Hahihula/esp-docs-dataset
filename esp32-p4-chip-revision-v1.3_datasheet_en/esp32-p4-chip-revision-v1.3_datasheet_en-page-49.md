**Title: Functional Description**

- **MWDTO:** HP core reset upon timeout
- **RWDT:** system reset upon timeout

**Write protection that makes WDT register read only unless unlocked**
- 32-bit timeout counter

**Clock source:**
- MWDT: PLL_F80M_CLK, RC_FAST_CLK or XTAL_CLK
- RWDT: LP_DYN_SLOW_CLK

---

**4.1.4.10 RTC Timer**

RTC Timer is an important module for implementing low power management of ESP32-P4. Based on a 48-bit readable counter, RTC Timer is mainly used as a system timer in low power mode when the timer peripheral in the HP system is unavailable. It also allows for configuring timer interrupts and logging the time when specific events happen in the system.

**Feature List**
- **48-bit counter**
- Time logging when one of the following events happens:
  - HP system reset
  - CPU enters stall state
  - CPU exits stall state
  - Crystal powers up
  - Crystal powers down

Time logging through register configuration:

- Occurrence time cached of the most recent two specific events
- Generation of interrupts at target times, which are configurable. It is also possible to configure two target times simultaneously.
- Uninterrupted operation during any reset or sleep mode, except for power-on reset of LP system.

---

**4.1.4.11 Permission Control (PMS)**

ESP32-P4 integrates an APM module to manage access permissions.

**Feature List**
- Up to 32 configurable address ranges for each DMA master
- Access permission management for each CPU core to access internal memory, external memory, and peripheral.
- Support for interrupts

---

*Espressif Systems*
*Submit Documentation Feedback*

ESP32-P4 Series Datasheet v0.6