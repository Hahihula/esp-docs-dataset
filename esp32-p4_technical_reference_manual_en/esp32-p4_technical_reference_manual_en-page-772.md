

```markdown
Chapter 11 Chip Boot Control

GoBack

Chapter 11

Chip Boot Control

11.1 Overview

Chip boot process and some chip functions are determined on power-on or hardware reset using strapping pins and eFuse bits. The following functionality can be determined:

*   chip boot mode
*   enable or disable of ROM messages printing
*   source of JTAG signals

ESP32-P4 has five strapping pins:

*   GPIO34
*   GPIO35
*   GPIO36
*   GPIO37
*   GPIO38

During Chip Reset (see Chapter 10 Reset and Clock), hardware samples and stores the voltage level of strapping pins as strapping bit of “0” or “1” in latches, and holds these bits until the chip is powered down. Software can read the latch status (strapping value) from GPIO_STRAPPING.

11.2 Functional Description

This section provides description of the chip functions and the patterns of the strapping pins and eFuse values to invoke each function.

Notice:
Only documented patterns should be used. If an undocumented pattern is used, it may trigger unexpected behaviors.

11.2.1 Default Configuration

By default, GPIO35 is connected to the chip’s internal pull-up resistor. If GPIO35 is not connected or is connected to an external high-impedance circuit, the internal weak pull-up determines the default input level of this strapping pin (see Table 11.2-1).
```