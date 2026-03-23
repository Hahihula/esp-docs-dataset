

```markdown
Chapter 9 Chip Boot Control

GoBack

Chapter 9

Chip Boot Control

9.1 Overview

Chip boot process and some chip functions are determined on power-on or hardware reset using strapping pins and eFuses. The following functionality can be determined:

- chip boot mode
- enable or disable of ROM messages printing to UART0
- source of JTAG signals
- SDIO input sampling edge and output driving edge

ESP32-C6 has five strapping pins:

- MTMS
- MTDI
- GPIO8
- GPIO9
- GPIO15

During Chip Reset (see Chapter 8 Reset and Clock), hardware captures samples and stores the voltage level of strapping pins as strapping bit of "0" or "1" in latches, and holds these bits until the chip is powered down or the next chip reset. Software can read the latch status (strapping value) from GPIO_STRAPPING.

9.2 Functional Description

This section provides description of the chip functions and the patterns of the strapping pins and eFuse values to invoke each function.

Notice:
Only documented patterns should be used. If an undocumented pattern is used, it may trigger unexpected behaviors.

9.2.1 Default Configuration

By default, GPIO9 is connected to the chip's internal pull-up resistor. If GPIO9 is not connected or is connected to an external high-impedance circuit, the internal weak pull-up determines the default input level of this strapping pin (see Table 9.2-1).
```