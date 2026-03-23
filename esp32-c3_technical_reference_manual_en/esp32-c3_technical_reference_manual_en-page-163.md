

```markdown
- Set `GPIO_PINx_SYNC1_BYPASS` to enable input signal synchronized on rising edge or on falling edge in the first clock, see Figure 5.4-1.
- Set `GPIO_PINx_SYNC2_BYPASS` to enable input signal synchronized on rising edge or on falling edge in the second clock, see Figure 5.4-1.

4. Configure IO MUX register to enable pin input. For this end, please set `IO_MUX_GPIOx_REG` corresponding to GPIO pin X as follows:
    - Set `IO_MUX_GPIOx_FUN_IE` to enable input².
    - Set or clear `IO_MUX_GPIOx_FUN_WPU` and `IO_MUX_GPIOx_FUN_WPD`, as desired, to enable or disable pull-up and pull-down resistors.

For example, to connect I2S MCLK input signal³ (I2S_MCLK_in, signal index 12) to GPIO7, please follow the steps below. Note that GPIO7 is also named as MTDO pin.

1. Set `GPIO_SIG12_IN_SEL` in register `GPIO_FUNC12_IN_SEL_CFG_REG` to enable peripheral signal input via GPIO matrix.
2. Set `GPIO_FUNC12_IN_SEL` in register `GPIO_FUNC12_IN_SEL_CFG_REG` to 7.
3. Set `IO_MUX_GPIO7_FUN_IE` in register `IO_MUX_GPIO7_REG` to enable pin input.

Note:
1. One input pin can be connected to multiple peripheral input signals.
2. The input signal can be inverted by configuring `GPIO_FUNCy_IN_INV_SEL`.
3. It is possible to have a peripheral read a constantly low or constantly high input value without connecting this input to a pin. This can be done by selecting a special `GPIO_FUNCy_IN_SEL` input, instead of a GPIO number:
    - When `GPIO_FUNCy_IN_SEL` is set to 0x1F, input signal is always 0.
    - When `GPIO_FUNCy_IN_SEL` is set to 0xE1, input signal is always 1.

5.4.4 Simple GPIO Input

GPIO_IN_REG holds the input values of each GPIO pin. The input value of any GPIO pin can be read at any time without configuring GPIO matrix for a particular peripheral signal. However, it is necessary to enable the input via IO MUX by setting `IO_MUX_GPIOx_FUN_IE` bit in register `IO_MUX_GPIOx_REG` corresponding to pin X, as mentioned in Section 5.4.2.

5.5 Peripheral Output via GPIO Matrix

5.5.1 Overview

To output a signal from a peripheral via GPIO matrix, the matrix is configured to route peripheral output signals (only signals with a name assigned in the column "Output signal" in Table 5.11-1) to one of the 22 GPIOs (0 ~ 21). See Table 5.11-1.

The output signal is routed from the peripheral into GPIO matrix and then into IO MUX. IO MUX must be configured to set the chosen pin to GPIO function. This enables the output GPIO signal to be connected to
```