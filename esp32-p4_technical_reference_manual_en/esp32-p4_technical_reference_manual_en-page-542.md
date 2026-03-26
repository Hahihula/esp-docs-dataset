

```markdown
Figure 9.4-3. Glitch Filter Timing Example

4. Synchronize GPIO input signals. To do so, please set `GPIO_PINx_REG` corresponding to GPIO pin X as follows:

* Set `GPIO_PINx_SYNC1_BYPASS` to enable input signal synchronized on rising edge or on falling edge in the first-level synchronization, see Figure 9.4-1.
* Set `GPIO_PINx_SYNC2_BYPASS` to enable input signal synchronized on rising edge or on falling edge in the second-level synchronization, see Figure 9.4-1.

5. Configure HP IO MUX register to enable pin input. For this end, please set `IO_MUX_GPIOx_REG` corresponding to GPIO pin X as follows:

* Set `IO_MUX_GPIOx_FUN_IE` to enable input².
* Set or clear `IO_MUX_GPIOx_FUN_WPU` and `IO_MUX_GPIOx_FUN_WPD` as desired to enable or disable pull-up and pull-down resistors.

For example, to connect UART0_TXD input signal³ (uart0_rxd_pad_in, signal index 10) to GPIO7, please follow the steps below.

1. Set `GPIO_SIG10_IN_SEL` in `GPIO_FUNC10_IN_SEL_CFG_REG` to enable peripheral signal input via HP GPIO matrix.
2. Set `GPIO_FUNC10_IN_SEL` in `GPIO_FUNC10_IN_SEL_CFG_REG` to 7, i.e., select GPIO7.
3. Set `IO_MUX_GPIO7_FUN_IE` in `IO_MUX_GPIO7_REG` to enable pin input.

Note:

1. One input pin can be connected to multiple peripheral input signals.
2. The input signal can be inverted by configuring `GPIO_FUNCy_IN_INV_SEL`.
3. It is possible to have a HP peripheral read a constantly low or constantly high input value without connecting this input to a pin. This can be done by selecting a special `GPIO_FUNCy_IN_SEL` input, instead of a GPIO number:

    * When `GPIO_FUNCy_IN_SEL` is set to 62, input signal is always 0.
    * When `GPIO_FUNCy_IN_SEL` is set to 63, input signal is always 1.

9.4.7.2 LP GPIO Matrix

The programming procedure for peripheral input via the LP GPIO matrix resembles that of Section 9.4.7.1. However, it's worth noting that:
```