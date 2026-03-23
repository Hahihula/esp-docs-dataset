

```markdown
Chapter 13 System Timer (SYSTIMER)		[GoBack]

Chapter 13

System Timer (SYSTIMER)

13.1 Overview

ESP32-C6 provides a 52-bit timer, which can be used to generate tick interrupts for the operating system, or be used as a general timer to generate periodic interrupts or one-time interrupts.

The timer consists of two counters: UNIT0 and UNIT1. The counter values can be monitored by three comparators COMP0, COMP1, and COMP2. See the timer block diagram on Figure 13.1-1.

![Figure 13.1-1. System Timer Structure](image_path_if_available)

13.2 Features

The system timer has the following features:

*   Two 52-bit counters and three 52-bit comparators
*   Software accessing registers clocked by APB_CLK
*   CNT_CLK used for counting, with an average frequency of 16 MHz in two counting cycles
*   40 MHz XTAL_CLK as the clock source of CNT_CLK
*   52-bit alarm values (t) and 26-bit alarm periods (δt)
*   Two modes to generate alarms:
    *   Target mode: only a one-time alarm is generated based on the alarm value (t)
    *   Period mode: periodic alarms are generated based on the alarm period (δt)

Espressif Systems	496 ESP32-C6 TRM (Version 1.1)
```