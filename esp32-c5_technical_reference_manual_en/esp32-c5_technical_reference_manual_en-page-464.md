

```markdown
Chapter 10 Chip Boot Control

GoBack

Chapter 10

Chip Boot Control

10.1 Overview

The chip allows for configuring the following boot parameters through strapping pins and eFuse parameters at power-up or a hardware reset, without microcontroller interaction.

*   Chip boot mode
    - Strapping pins: GPIO26, GPIO27, and GPIO28
*   SDIO sampling and driving clock edge
    - Strapping pins: GPIO25 and MTDI
*   ROM messages printing
    - Strapping pin: GPIO27
    - eFuse parameters: EFUSE_UART_PRINT_CONTROL and EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT
*   JTAG signal source
    - Strapping pin: GPIO7
    - eFuse parameters: EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE

The default values of all the above eFuse parameters are 0, which means that they are not burnt. Given that eFuse is one-time programmable, once an eFuse bit is programmed to 1, it can never be reverted to 0. For how to program eFuse bits, please refer to Chapter 7 eFuse Controller (EFUSE).

During Chip Reset (see Chapter 9 Reset and Clock), hardware captures samples and stores the voltage level of strapping pins as strapping bit of "0" or "1" in latches, and holds these bits until the chip is powered down or next chip reset. Software can read the latch status (strapping value) from GPIO_STRAPPING.

10.2 Functional Description

This section introduces chip reset functions and the patterns of the strapping pins and eFuse values to invoke each function.

Notice: Only documented patterns should be used. If an undocumented pattern is used, it may trigger unexpected behaviors.
```