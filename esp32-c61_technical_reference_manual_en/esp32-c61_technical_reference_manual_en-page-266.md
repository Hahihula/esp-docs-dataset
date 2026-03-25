

```markdown
## 6.11.1 Power Supplies of GPIO Pins

For more information on the power supply for GPIO pins, please refer to Pin Definition in ESP32-C61 Datasheet. All the pins can be used to wake up the chip from Light-sleep, but only the pins (GPIO0~GPIO6) in VDDPST1 domain can be used to wake up the chip from Deep-sleep.

## 6.11.2 Power Supply Management

Each ESP32-C61 pin is connected to one of the following power domains.
*   VDDPST1: the input power supply for LP GPIO pins
*   VDDPST2: the input power supply for HP GPIO pins

## 6.12 HP Peripheral Signal List

Table 6.12-1 shows the peripheral input/output signals via HP GPIO matrix.

Please pay attention to the configuration of the bit GPIO_FUNCn_OE_SEL:

*   `GPIO_FUNCn_OE_SEL = 1`: the output enable is controlled by the corresponding bit n of GPIO_ENABLE_REG:
    -   `GPIO_ENABLE_REG = 0`: output is disabled.
    -   `GPIO_ENABLE_REG = 1`: output is enabled.

*   `GPIO_FUNCn_OE_SEL = 0`: use the output enable signal from peripheral, for example FSPIQ_oe in the column "Output enable signal when GPIO_FUNCn_OE_SEL = 0" of Table 6.12-1. Note that the signals such as FSPIQ_oe can be 1 ('d1) or 0 ('d0), depending on the configuration of corresponding peripherals. If it's 1'd1 in column "Output enable signal when GPIO_FUNCn_OE_SEL = 0", it indicates that once GPIO_FUNCn_OE_SEL is cleared, the output signal is always enabled by default.

**Note:**
Signals are numbered consecutively, but not all signals are valid. Only the signals with a name assigned in the column "Input signal" or in the column "Output signal" in Table 6.12-1 are valid input or output signals.
```

```markdown
Table 6.12-1. Peripheral Signals via HP GPIO Matrix

| Signal No. | Input Signal   | Default Value | Direct Input via HP IO MUX | Output Signal           | Output Enable Signal when GPIO_FUNCn_OE_SEL = 0 | Direct Output via HP IO MUX |
|------------|----------------|---------------|----------------------------|-------------------------|---------------------------------------------|------------------------------|
| 0          | —              | -             | -                          | ledc_is_sig_out0       | 1'd1                                       | no                            |
| 1          | —              | —             | —                          | ledc_is_sig_out1       | 1'd1                                       | no                            |
| 2          | —              | —             | —                          | ledc_is_sig_out2       | 1'd1                                       | no                            |
| 3          | —              | —             | —                          | ledc_is_sig_out3       | 1'd1                                       | no                            |
| 4          | —              | —             | —                          | ledc_is_sig_out4       | 1'd1                                       | no                            |
| 5          | —              | —             | —                          | ledc_is_sig_out5       | 1'd1                                       | no                            |
| 6          | UORXD_in        | 0             | yes                        | UOTXD_out              | 1'd1                                       | yes                           |
```