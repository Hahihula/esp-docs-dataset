
```markdown
## 6.8 Pin Functions in Light-sleep

Pins may provide different functions when ESP32-H2 is in Light-sleep mode. If IO_MUX_GPIOn_SLP_SEL in register IO_MUX_GPIOn_REG for a GPIO pin is set to 1, a different set of bits will be used to control the pin when the chip is in Light-sleep mode.

Table 6.8-1. Bit Used to Control IO MUX Functions in Light-sleep Mode

| IO MUX Function                  | Normal Execution OR IO_MUX_GPIOn_SLP_SEL = 0 | Light-sleep Mode AND IO_MUX_GPIOn_SLP_SEL = 1 |
|----------------------------------|---------------------------------------------|------------------------------------------------|
| Output Drive Strength            | IO_MUX_GPIOn_FUN_DRV                        | IO_MUX_GPIOn_MCU_DRV                           |
| Pull-up Resistor                 | IO_MUX_GPIOn_FUN_WPU                        | IO_MUX_GPIOn_MCU_WPU                            |
| Pull-down Resistor               | IO_MUX_GPIOn_FUN_WPD                        | IO_MUX_GPIOn_MCU_WPD                            |
| Input Enable                     | IO_MUX_GPIOn_FUN_IE                         | IO_MUX_GPIOn_MCU_IE                             |
| Output Enable                    | OEN_SEL from GPIO matrix *                  | IO_MUX_GPIOn_MCU_OE                              |

*Note:*
If IO_MUX_GPIOn_SLP_SEL is set to 0, pin functions remain the same in both normal execution and in Light-sleep mode. Please refer to Section 6.5.2 for how to enable output in normal execution.

## 6.9 Pin Hold Feature

Each GPIO pin (including the LP pins: GPIO8 ~ GPIO14) has an individual hold function controlled by an LP register. When the pin is set to hold, the state is latched at that moment and will not change no matter how the internal signals change or how the IO MUX/GPIO configuration is modified. Users can use the hold function for the pins to retain the pin state through a core reset triggered by watchdog time-out or Deep-sleep events.

To use this feature, follow the steps below:

- Digital pins (GPIO0 ~ GPIO5, GPIO22 ~ GPIO27):
  - To maintain pin input/output status in Deep-sleep mode, users can set LP_AON_GPIO_HOLD0_REG[n] to 1 before powering down. To disable the hold function after the chip is woken up, users can set LP_AON_GPIO_HOLD0_REG[n] to 0.
  - Or users can set PMU_TIE_HIGH_HP_PAD_HOLD_ALL to maintain the input/output status of all digital pins, and set PMU_TIE_LOW_HP_PAD_HOLD_ALL to disable the hold function of all digital pins.

- LP pins (GPIO8 ~ GPIO14):
  - The input and output values of LP GPIO pins are controlled by LP_AON_GPIO_HOLDO_REG[n], PMU_TIE_HIGH_LP_PAD_HOLD_ALL, and PMU_TIE_LOW_LP_PAD_HOLD_ALL. Users can set LP_AON_GPIO_HOLDO_REG[n] to 1 to hold the value of GPIOn, or set LP_AON_GPIO_HOLDO_REG[n] to 0 to disable the hold function of GPIOn.
```