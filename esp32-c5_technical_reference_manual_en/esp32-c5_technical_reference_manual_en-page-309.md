

```markdown
- Configure GPIO_EXT_FILTER_CHn_INPUT_IO_NUM to m. n (0~7) represents the channel number.
m (0~14, 23~28) represents the GPIO pin number.

- Configure GPIO_EXT_FILTER_CHn_WINDOW_WIDTH to VALUE1 and
GPIO_EXT_FILTER_CHn_WINDOW_THRESH to VALUE2. During VALUE1 + 1 cycles, if there are VALUE2
+ 1 input signals that do not match the current output signal value, the Glitch Filter hardware inverts
the output signal. GPIO_EXT_FILTER_CHn_WINDOW_WIDTH and
GPIO_EXT_FILTER_CHn_WINDOW_THRESH can be configured to the same value VALUE3, then only
signals with a width greater than VALUE3 + 1 clock cycles will be sampled.

- Set GPIO_EXT_FILTER_CHn_EN to enable channel n.
```

An example is shown in Figure 8.4-3, where GPIO_EXT_FILTER_CHn_WINDOW_WIDTH is configured to 3 and GPIO_EXT_FILTER_CHn_WINDOW_THRESH to 2. The output signal value (signal_out) keeps as “0” in the four clock cycles before T1. The input signal value (signal_in) has been “1” for three clock cycles in the same period, then the output signal is inverted to “1” after T1.

![Figure 8.4-3. Glitch Filter Timing Example](image)

```markdown
4. Synchronize GPIO input signals. To do so, please set GPIO_PINx_REG corresponding to GPIO pin X as follows:

- Set GPIO_PINx_SYNC1_BYPASS to enable input signal synchronized on rising edge or on falling edge in the first-level synchronization, see Figure 8.4-1.

- Set GPIO_PINx_SYNC2_BYPASS to enable input signal synchronized on rising edge or on falling edge in the second-level synchronization, see Figure 8.4-1.
```

```markdown
5. Configure HP IO MUX register to enable pin input. For this end, please set IO_MUX_GPIOx_REG corresponding to GPIO pin X as follows:

- Set IO_MUX_GPIOx_FUN_IE to enable input²³.

- Set or clear IO_MUX_GPIOx_FUN_WPU and IO_MUX_GPIOx_FUN_WPD as desired to enable or disable pull-up and pull-down resistors.
```

**Note:**

1. One input pin can be connected to multiple peripheral input signals.
2. The input signal can be inverted by configuring GPIO_FUNCy_IN_INV_SEL.
3. It is possible to have an HP peripheral read a constantly low or constantly high input value without connecting this input to a pin. This can be done by selecting a special GPIO_FUNCy_IN_SEL input, instead of a GPIO number:
```