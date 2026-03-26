

```markdown
## 9.8 Pin Functions in Light-sleep

Pins may provide different functions when ESP32-P4 is in Light-sleep mode. If IO_MUX_GPIOn_SLP_SEL in register IO_MUX_GPIOn_REG for a GPIO pin is set to 1, a different set of bits will be used to control the pin when the chip is in Light-sleep mode.

Table 9.8-1. Bit Used to Control IO MUX Functions in Light-sleep Mode

| IO MUX Function | Normal Execution OR IO_MUX_GPIOn_SLP_SEL = 0 | Light-sleep Mode AND IO_MUX_GPIOn_SLP_SEL = 1 |
|-----------------|---------------------------------------------|-----------------------------------------------|
| Output Drive Strength | IO_MUX_GPIOn_FUN_DRV                        | IO_MUX_GPIOn_MCU_DRV                          |
| Pull-up Resistor   | IO_MUX_GPIOn_FUN_WPU                         | IO_MUX_GPIOn_MCU_WPU                          |
| Pull-down Resistor | IO_MUX_GPIOn_FUN_WPD                         | IO_MUX_GPIOn_MCU_WPD                          |
| Input Enable       | IO_MUX_GPIOn_FUN_IE                          | IO_MUX_GPIOn_MCU_IE                           |
| Output Enable      | OE_SEL from GPIO matrix*                     | IO_MUX_GPIOn_MCU_OE                            |

Note:
If IO_MUX_GPIOn_SLP_SEL is set to 0, pin functions remain the same in both normal execution and in Light-sleep mode. Please refer to Section 9.5.4.1 for how to enable output in normal execution.

## 9.9 Pin Hold Feature

Each GPIO pin has an individual hold function controlled by Power Management Unit (PMU) or registers. When the pin is set to hold, the state is latched at that moment and will not change no matter how the internal signals change or how the IO MUX/GPIO configuration is modified. Users can use the hold function for the pins to retain the pin state through a core reset triggered by watchdog time-out or Deep-sleep events.

HP Pins (GPIO16 ~ GPIO54):

The Hold state of each HP pin is controlled by the result of OR operation of the pin's Hold enable signal and the global Hold enable signal.

- Each pin's Hold enable signal is controlled by the following registers:

  - In Deep-sleep mode:
    * LP_SYSTEM_REG_PAD_RTC_HOLD_CTRL0[n] (n = 16~31), controls the Hold signal of each pin of GPIO16~GPIO31.
    * LP_SYSTEM_REG_PAD_RTC_HOLD_CTRL1[n] (n = 0~22), controls the Hold signal of each pin of GPIO32~GPIO54.

  - In non-Deep-sleep mode:
    * HP_SYSTEM_GPIO_O_HOLD_LOW[n] (n = 0~31), controls the Hold signal of each pin of GPIO16~GPIO47.
    * HP_SYSTEM_GPIO_O_HOLD_HIGH[n](n = 0~6), controls the Hold signal of each pin of GPIO48~GPIO54.
```