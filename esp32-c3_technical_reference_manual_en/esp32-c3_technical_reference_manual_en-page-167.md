

```markdown
## 5.8 Pin Functions in Light-sleep

Pins may provide different functions when ESP32-C3 is in Light-sleep mode. If IO_MUX_SLP_SEL in register `IO_MUX_n_REG` for a GPIO pin is set to 1, a different set of bits will be used to control the pin when the chip is in Light-sleep mode.

Table 5.8-1. Bits Used to Control IO MUX Functions in Light-sleep Mode

| IO MUX Functions | Normal Execution OR `IO_MUX_SLP_SEL = 0` | Light-sleep Mode AND `IO_MUX_SLP_SEL = 1` |
|------------------|------------------------------------------|-------------------------------------------|
| Output Drive Strength | `IO_MUX_FUN_DRV`                        | `IO_MUX_MCU_DRV`                          |
| Pull-up Resistor    | `IO_MUX_FUN_WPU`                        | `IO_MUX_MCU_WPU`                          |
| Pull-down Resistor  | `IO_MUX_FUN_WPD`                        | `IO_MUX_MCU_WPD`                          |
| Output Enable       | `OEN_SEL from GPIO matrix *`            | `IO_MUX_MCU_OE`                           |

*Note:*
If `IO_MUX_SLP_SEL` is set to 0, pin functions remain the same in both normal execution and Light-sleep mode. Please refer to Section 5.5.2 for how to enable output in normal execution.

## 5.9 Pin Hold Feature

Each GPIO pin (including the RTC pins: GPIO0 ~ GPIO5) has an individual hold function controlled by a RTC register. When the pin is set to hold, the state is latched at that moment and will not change no matter how the internal signals change or how the IO MUX/GPIO configuration is modified. Users can use the hold function for the pins to retain the pin state through a core reset triggered by watchdog time-out or Deep-sleep events.

*Note:*
- For digital pins (GPIO6 ~21), to maintain pin input/output status in Deep-sleep mode, users can set `RTC_CNTL_DIG_PAD_HOLDn` in register `RTC_CNTL_DIG_PAD_HOLD_REG` to 1 before powering down. To disable the hold function after the chip is woken up, users can set `RTC_CNTL_DIG_PAD_HOLDn` to 0.
- For RTC pins (GPIO0 ~5), the input and output values are controlled by the corresponding bits of register `RTC_CNTL_PAD_HOLD_REG`, and users can set it to 1 to hold the value or set it to 0 to unhold the value.

## 5.10 Power Supplies and Management of GPIO Pins

### 5.10.1 Power Supplies of GPIO Pins

For more information on the power supply for GPIO pins, please refer to Pin Definition in ESP32-C3 Datasheet. All the pins can be used to wake up the chip from Light-sleep mode, but only the pins (GPIO0 ~ GPIO5) in VDD3P3_RTC domain can be used to wake up the chip from Deep-sleep mode.
```