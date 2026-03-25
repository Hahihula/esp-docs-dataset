

```markdown
## 6.9 Pin Hold Feature

Each GPIO pin has an individual hold function controlled by Power Management Unit (PMU) or registers. When the pin is set to hold, the state is latched at that moment and will not change no matter how the internal signals change or how the IO MUX/GPIO configuration is modified. Users can use the Hold function for the pins to retain the pin state through a core reset triggered by watchdog time-out or Deep-sleep events.

The Hold state of each GPIO pin is controlled by the result of OR operation of the pin’s Hold enable signal and the global Hold enable signal.

- Hold signal of each individual pin:
  - `LP_AON_GPIO_HOLD0_REG[n]` (n = 0~13, 22~29) controls the Hold signal of each pin.
- Global Hold signal:

  - Global Hold signal of HP GPIO pins:
    * `PMU_TIE_HIGH_HP_PAD_HOLD_ALL`: enables the global Hold signal of all HP GPIO pins.
    * `PMU_TIE_LOW_HP_PAD_HOLD_ALL`: disables the global Hold signal of all HP GPIO pins.

  - Global Hold signal of LP GPIO pins:
    * `PMU_TIE_HIGH_LP_PAD_HOLD_ALL`: enables the global Hold signal of all LP GPIO pins.
    * `PMU_TIE_LOW_LP_PAD_HOLD_ALL`: disables the global Hold signal of all LP GPIO pins.

Enable or disable the Hold feature of the pins by one of the following ways:

- **Method 1:** enable or disable the Hold feature of individual pins:
  To maintain the pin’s input/output status in Deep-sleep, set `LP_AON_GPIO_HOLD0_REG[n]` (where n = 0~13, 22~29 corresponds to GPIO0~GPIO13, GPIO22~GPIO29). To disable the hold function after waking up, clear the bit[n].

- **Method 2:** enable or disable the Hold feature of all HP/LP pins:

  - HP Pins
    Set `PMU_TIE_HIGH_HP_PAD_HOLD_ALL` to maintain the input/output status of all HP pins and set `PMU_TIE_LOW_HP_PAD_HOLD_ALL` to disable the hold function for all HP pins.

  - LP Pins
    Set `PMU_TIE_HIGH_LP_PAD_HOLD_ALL` to maintain the input/output status of all LP pins and set `PMU_TIE_LOW_LP_PAD_HOLD_ALL` to disable the hold function for all LP pins.

- **Method 3:** Use PMU Task
  Configure the PMU task to hold the HP pins before Deep-sleep. In Deep-sleep, the HP pins would be hold automatically by the PMU.

## 6.10 Hysteresis Characteristics

Each GPIO pin has hysteresis functionality. When hysteresis is not enabled, as shown in Figure 6.10-1, the level flip of the signal (C) input to the chip from the PAD has only one threshold (Vt, about 1.7 V). When the voltage on the PAD is higher than Vt, the level on the C is high. Otherwise, it is low. However, noise on the PAD may affect the signal on C.
```