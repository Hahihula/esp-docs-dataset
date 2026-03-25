

```markdown
Chapter 8 Chip Boot Control

GoBack

Chapter 8

Chip Boot Control

8.1 Overview

Chip boot process and some chip functions are determined on power-on or hardware reset by strapping pins and eFuse parameters. The following functionality can be determined:

*   Chip boot mode
    -   Strapping pins: GPIO8 and GPIO9
*   SDIO sampling and driving clock edge
    -   Strapping pins: MTDI and MTMS
*   UARTO/USB ROM message printing
    -   Strapping pin: GPIO8
    -   eFuse parameters: EFUSE_UART_PRINT_CONTROL and EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT
*   JTAG signal source
    -   Strapping pin: GPIO7
    -   eFuse parameters: EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE

The default values of all the above eFuse parameters are 0, which means that they are not burnt. Given that eFuse is one-time programmable, once programmed to 1, it can never be reverted to 0. For how to program eFuse parameters, please refer to Chapter 5 eFuse Controller (EFUSE).

During power-on reset, and brownout reset (see Chapter 7 Reset and Clock), hardware captures samples and stores the voltage level of strapping pins as strapping bit of “0” or “1” in latches, and holds these bits until the chip is powered down or next chip reset. Software can read the latch status (strapping value) from GPIO_STRAPPING.

8.2 Functional Description

This section introduces chip reset functions and the patterns of the strapping pins and eFuse values used to invoke each function.

Notice: Only documented patterns should be used. Undocumented patterns may trigger unexpected behaviors.
```