

```markdown
Chapter 8
Chip Boot Control

8.1 Overview

Chip boot process and some chip functions are determined on power-on or hardware reset by strapping pins and eFuses. The following functionality can be determined:

- chip boot mode
- enable or disable ROM messages printing to UARTO/USB
- source of JTAG signals

ESP32-H2 has three strapping pins:
- GPIO8
- GPIO9
- GPIO25

During Chip Reset (see Chapter 7 Reset and Clock), hardware captures samples and stores the voltage level of strapping pins as strapping bit of "0" or "1" in latches, and holds these bits until the chip is powered down or next chip reset. Software can read the latch status (strapping value) from GPIO_STRAPPING.

8.2 Functional Description

This section introduces chip reset functions and the patterns of the strapping pins and eFuse values to invoke each function.

Notice:
Only documented patterns should be used. If an undocumented pattern is used, it may trigger unexpected behaviors.

8.2.1 Default Configuration

By default, GPIO9 is connected to the chip's internal pull-up resistor. If GPIO9 is not connected or is connected to an external high-impedance circuit, the internal weak pull-up determines the default input level of this strapping pin (see Table 8.2-1).
```