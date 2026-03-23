

```markdown
- Write 1 to the corresponding bit in LP_GPIO_ENABLE_W1TC, to clear output enable.

See Table 7.13-2 for analog functions of LP GPIO pins.
```

## 7.8 Pin Functions in Light-sleep

Pins may provide different functions when ESP32-C6 is in Light-sleep mode. If IO_MUX_GPIOn_SLP_SEL in register IO_MUX_GPIOn_REG for a GPIO pin is set to 1, a different set of bits will be used to control the pin when the chip is in Light-sleep mode.

Table 7.8-1. Bit Used to Control IO MUX Functions in Light-sleep Mode

| IO MUX Function | Normal Execution OR IO_MUX_GPIOn_SLP_SEL = 0 | Light-sleep Mode AND IO_MUX_GPIOn_SLP_SEL = 1 |
|-----------------|---------------------------------------------|------------------------------------------------|
| Output Drive Strength | IO_MUX_GPIOn_FUN_DRV                       | IO_MUX_GPIOn_MCU_DRV                          |
| Pull-up Resistor     | IO_MUX_GPIOn_FUN_WPU                        | IO_MUX_GPIOn_MCU_WPU                          |
| Pull-down Resistor   | IO_MUX_GPIOn_FUN_WPD                        | IO_MUX_GPIOn_MCU_WPD                          |
| Input Enable         | IO_MUX_GPIOn_FUN_IE                         | IO_MUX_GPIOn_MCU_IE                           |
| Output Enable        | QEN_SEL from GPIO matrix *                  | IO_MUX_GPIOn_MCU_OE                            |

*Note:*
If IO_MUX_GPIOn_SLP_SEL is set to 0, pin functions remain the same in both normal execution and in Light-sleep mode. Please refer to Section 7.5.2 for how to enable output in normal execution.

## 7.9 Pin Hold Feature

Each GPIO pin (including the LP pins: GPIO0 ~ GPIO7) has an individual hold function controlled by an LP register. When the pin is set to hold, the state is latched at that moment and will not change no matter how the internal signals change or how the IO MUX/GPIO configuration is modified. Users can use the hold function for the pins to retain the pin state through a core reset triggered by watchdog time-out or Deep-sleep events.

To use this feature, follow the steps below:

- Digital pins (GPIO8 ~ GPIO30)
  The Hold state of each digital pin is controlled by the result of OR operation of the pin's Hold enable signal and the global Hold enable signal.
    - LP_AON_GPIO_HOLD_REG[n] (n = 8 ~ 30), controls the Hold signal of each pin of GPIO8 ~ GPIO30.
    - PMU_TIE_HIGH_HP_PAD_HOLD_ALL, controls the global Hold signal of all digital pins.

To use this feature, follow the steps below:
- To maintain pin input/output status in Deep-sleep mode, users can set LP_AON_GPIO_HOLD_REG[n] (where n = 8 ~ 30 corresponds to GPIO8 ~ GPIO30) to 1 before
```