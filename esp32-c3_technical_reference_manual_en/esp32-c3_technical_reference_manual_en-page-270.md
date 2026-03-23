

```markdown
Chapter 10 System Timer (SYSTIMER)

GoBack

Chapter 10

System Timer (SYSTIMER)

10.1 Overview

ESP32-C3 provides a 52-bit timer, which can be used to generate tick interrupts for operating system, or be used as a general timer to generate periodic interrupts or one-time interrupts.

The timer consists of two counters UNITO and UNIT1. The count values can be monitored by three comparators COMPO, COMP1 and COMP2. See the timer block diagram on Figure 10.1-1.

![Figure 10.1-1. System Timer Structure](image_path_if_available)

10.2 Features

*   Consist of two 52-bit counters and three 52-bit comparators
*   Software accessing registers is clocked by APB_CLK
*   Use CNT_CLK for counting, with an average frequency of 16 MHz in two counting cycles
*   Use 40 MHz XTAL_CLK as the clock source of CNT_CLK
*   Support for 52-bit alarm values (t) and 26-bit alarm periods (δt)
*   Provide two modes to generate alarms:
    *   Target mode: only a one-time alarm is generated based on the alarm value (t)
    *   Period mode: periodic alarms are generated based on the alarm period (δt)
*   Three comparators can generate three independent interrupts based on configured alarm value (t) or alarm period (δt)

Espressif Systems
270
ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback
```