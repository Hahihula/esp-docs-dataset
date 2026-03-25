

```markdown
- When `GPIO_FUNCy_IN_SEL` is set to `0x40`, input signal is always `0`.
- When `GPIO_FUNCy_IN_SEL` is set to `0x60`, input signal is always `1`.

Programming Example
To connect UARTO RXD input signal (UORXD_in, signal index 6) to GPIO7, please follow the steps below.
1. Set `GPIO_SIG6_IN_SEL` in `GPIO_FUNC6_IN_SEL_CFG_REG` to enable peripheral signal input via HP GPIO matrix.
2. Set `GPIO_FUNC6_IN_SEL` in `GPIO_FUNC6_IN_SEL_CFG_REG` to `7`, i.e., select GPIO7.
3. Set `IO_MUX_GPIO7_FUN_IE` in `IO_MUX_GPIO7_REG` to enable pin input.

8.4.7.2 LP GPIO Matrix
For inputs, LP GPIO matrix only supports the GPIO wakeup function. For LP GPIO input wakeup programming, please refer to Section 8.4.6.2.

8.5 Peripheral Output via GPIO Matrix

8.5.1 Overview
To output a signal from a peripheral via GPIO matrix:
- Configure the HP GPIO matrix to route HP peripheral output signals (only signals with a name assigned in the column “Output signal” in Table 8.12-1) to one of the 21 GPIOs (`0~14`, `23~28`).
- Then the output signal is routed from the peripheral into GPIO matrix and then into IO MUX. IO MUX must be configured to set the chosen pin to GPIO function. This enables the GPIO output signal to be connected to the pin.

For the detailed programming procedure, see Section 8.5.4.1.

Note:
There is a range of peripheral output signals (`97~100` in Table 8.12-1) which are not connected to any peripheral, but to the input signals (`97~100`) directly.

8.5.2 Simple GPIO Output
GPIO matrix can also be used for simple GPIO output. For this case, one GPIO pin can be configured to directly output the desired value, without routing any peripheral output to this pin.
Follow the steps below to configure HP GPIO matrix for simple GPIO output:
- Set `GPIO_FUNCx_OUT_SEL` with a special peripheral index `256 (0x100)`.
- Configure the corresponding bit in `GPIO_OUT_REG` to the desired GPIO output value.

Note:
- The bits `GPIO_OUT_REG[0~14, 23~28]` correspond to `GPIO0~GPIO14`, `GPIO23~GPIO28`.
- Recommended operation: use `GPIO_OUT_W1TS` and `GPIO_OUT_W1TC` to set or clear `GPIO_OUT_REG`.
```