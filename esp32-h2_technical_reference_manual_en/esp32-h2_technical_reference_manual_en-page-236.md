

```markdown
- `1*` - If `EFUSE_DIS_PAD_JTAG = 1`, the pin MTCK is left floating after reset, i.e., `IE = 1`. If `EFUSE_DIS_PAD_JTAG = 0`, the pin MTCK is connected to internal pull-up resistor, i.e., `IE = 1`, `WPU = 1`.
- `3*` - `IE = 1`, `WPU = 0`. The default value of GPIO27's USB pull-up is 1, which means the pull-up resistor is enabled. For details, please refer to the note below.

## GPIO Input Mode

The input function of GPIO can be configured as hysteresis or normal mode:

- Hysteresis mode: In the hysteresis mode, the threshold voltage for flipping between high and low levels of GPIO input depends on the direction of level flipping. Specifically, the voltage threshold for flipping from high to low level is slightly lower than the voltage threshold for flipping from low to high level. For details, see Chapter 6.10.
- Normal mode: Disable hysteresis for GPIO pins, and the threshold voltage for flipping between high and low levels of GPIO input is independent of the direction of level flipping. In other words, the voltage threshold for flipping from high to low level is the same as the voltage threshold for flipping from low to high level.

**Note:**
- `R` - LP pins. Some LP pins have analog functions. For details, see 6.14-1.
- `USB` - USB pull-up resistor enabled
    - By default, the USB function is enabled for USB pins (i.e., GPIO26 and GPIO27), and the pin pull-up is decided by the USB pull-up. The USB pull-up is controlled by `USB_SERIAL_JTAG_DP/DM_PULLUP` and the pull-up resistor value is controlled by `USB_SERIAL_JTAG_PULLUP_VALUE`. For details, see [ESP32-H2 Technical Reference Manual > Chapter USB Serial/JTAG Controller](#).
    - When the USB function is disabled, USB pins are used as regular GPIOs and the pin's internal weak pull-up and pull-down resistors are disabled by default (configurable by `IO_MUX_GPIOn_MCU_WPU/WPD`).

## 6.14 IO MUX Pins Analog Functions List

Table 6.14-1 lists all the IO MUX pins that have analog functions.

**Table 6.14-1. Analog Functions of IO MUX Pins**

| GPIO No.<sup>1</sup> | Pin Name   | Analog Function 0 | Analog Function 1 |
|----------------------|------------|-------------------|-------------------|
| 1                    | GPIO1      | -                 | ADC1_CH0          |
| 2                    | MTMS       | -                 | ADC1_CH1          |
| 3                    | MTDO       | -                 | ADC1_CH2          |
| 4                    | MTCK       | -                 | ADC1_CH3          |
| 5                    | MTDI       | -                 | ADC1_CH4          |
| 10                   | GPIO10     | ZCD<sup>1</sup>    | -                 |
| 11                   | GPIO11     | ZCD<sup>1</sup>    | -                 |
| 13                   | XTAL_32K_P | XTAL_32K_P        | -                 |
| 14                   | XTAL_32K_N | XTAL_32K_N        | -                 |
```