

```markdown
Figure 9.10-2. Example of Level Flip on the Chip Pad — Hysteresis Function Enabled

9.11 Power Supplies and Management of GPIO Pins

9.11.1 Power Supplies of GPIO Pins

For more information on the power supply for GPIO pins, please refer to Pin Definition in ESP32-P4 Datasheet.
All the pins can be used to wake up the chip from Light-sleep, but only the pins (GPIO0 ~ GPIO15) in VDD_LP domain can be used to wake up the chip from Deep-sleep.

9.11.2 Power Supply Management

Each ESP32-P4 pin is connected to one of the following power domains.
*   VDD_LP: the input power supply for LP GPIO pins
*   VDD_IO_0, VDD_FLASHIO, VDD_IO_4 ~ VDD_IO_6: the input power supply for HP GPIO pins

9.12 HP Peripheral Signal List

Table 9.12-1 shows the peripheral input/output signals via HP GPIO matrix.

Please pay attention to the configuration of the bit GPIO_FUNCn_OE_SEL:

*   GPIO_FUNCn_OE_SEL = 1: the output enable is controlled by the corresponding bit n of GPIO_ENABLE/ENABLE1_REG:
    -   GPIO_ENABLE/ENABLE1_REG = 0: output is disabled.
    -   GPIO_ENABLE/ENABLE1_REG = 1: output is enabled.
*   GPIO_FUNCn_OE_SEL = 0: use the output enable signal from peripheral, for example spi2_dqs_pad_oe in the column “Output enable signal when GPIO_FUNCn_OE_SEL = 0” of Table 9.12-1. Note that the signals such as spi2_dqs_pad_oe can be 1 (1’d1) or 0 (1’d0), depending on the configuration of corresponding peripherals. If it’s 1’d1 in column “Output enable signal when GPIO_FUNCn_OE_SEL = 0”, it indicates that once GPIO_FUNCn_OE_SEL is cleared, the output signal is always enabled by default.

Note:
Signals are numbered consecutively, but not all signals are valid.
*   Only the signals with a name assigned in the column “Input signal” in Table 9.12-1 are valid input signals.
*   Only the signals with a name assigned in the column “Output signal” in Table 9.12-1 are valid output signals.
```