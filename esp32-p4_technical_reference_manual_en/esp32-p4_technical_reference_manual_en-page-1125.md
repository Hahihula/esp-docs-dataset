
```markdown
Chapter 18 RTC Timer

RTC Timer is an important module for implementing low power management of ESP32-P4. Based on a 48-bit readable counter, RTC Timer is mainly used as a system timer in low power mode when the timer peripheral in the HP system is unavailable. It also allows for configuring timer interrupts and logging the time when specific events happen in the system. The supported events are described in the 18.3 Functional Description.

18.2 Feature List

RTC Timer has the following features:

*   48-bit counter
*   Time logging when one of the following events happens:
    *   HP system reset
    *   CPU enters stall state
    *   CPU exits stall state
    *   Crystal powers up
    *   Crystal powers down
*   Time logging through register configuration
*   Occurrence time cached of the most recent two specific events
*   Generation of interrupts at target times, which are configurable. It is also possible to configure two target times simultaneously.
*   Uninterrupted operation during any reset or sleep mode, except for power-on reset of LP system.

18.3 Functional Description

*   48-bit counter
    *   The implementation of the RTC Timer is based on a 48-bit counter, driven by the RC_SLOW_CLK in the AlwaysOn power domain. It uses continuous loop counting (except during LP system reset), and an overflow interrupt is generated when the 48-bit counter overflows.
*   Log the occurrence time of specific events
    *   RTC Timer supports logging the occurrence time of three types of events:
```