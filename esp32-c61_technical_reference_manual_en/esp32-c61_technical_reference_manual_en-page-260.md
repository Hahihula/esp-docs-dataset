

```markdown
Chapter 6 GPIO Matrix and IO MUX GoBack

1. Set `GPIO_SIG6_IN_SEL` in `GPIO_FUNC6_IN_SEL_CFG_REG` to enable peripheral signal input via HP GPIO matrix.
2. Set `GPIO_FUNC6_IN_SEL` in `GPIO_FUNC6_IN_SEL_CFG_REG` to 7, i.e., select GPIO7.
3. Set `IO_MUX_GPIO7_FUN_IE` in `IO_MUX_GPIO7_REG` to enable pin input.

6.4.6.2 LP GPIO Matrix

For inputs, LP GPIO matrix only supports the GPIO wakeup function. For LP GPIO input wakeup programming, please refer to Section 6.4.5.2.

6.5 Peripheral Output via GPIO Matrix

6.5.1 Overview

To output a signal from a peripheral via HP GPIO matrix:

- Configure the HP GPIO matrix to route HP peripheral output signals (only signals with a name assigned in the column “Output signal” in Table 6.12-1) to one of the 22 GPIOs (0~13, 22~29).
- Then the output signal is routed from the peripheral into HP GPIO matrix and then into HP IO MUX. HP IO MUX must be configured to set the chosen pin to GPIO function. This enables the GPIO output signal to be connected to the pin.

For the detailed programming procedure, see Section 6.5.3.1.

Note:
There is a range of peripheral output signals (97~100 in Table 6.12-1) which are not connected to any peripheral, but to the input signals (97~100) directly.

6.5.2 Simple GPIO Output

GPIO matrix can also be used for simple GPIO output. For this case, one GPIO pin can be configured to directly output the desired value, without routing any peripheral output to this pin.

Follow the steps below to configure HP GPIO matrix for simple GPIO output:

- Set `GPIO_FUNCx_OUT_SEL` with a special peripheral index 256 (0x100).
- Configure the corresponding bit in `GPIO_OUT_REG` to the desired GPIO output value.

Note:
- The bits `GPIO_OUT_REG[0~13, 22~29]` correspond to GPIO0~GPIO13, GPIO22~GPIO29.
- Recommended operation: use `GPIO_OUT_W1TS` and `GPIO_OUT_W1TC` to set or clear `GPIO_OUT_REG`.

LP GPIO matrix supports only the Simple GPIO Output function. There is no need to configure function selection registers. Just configure the corresponding bit in `LP_GPIO_OUT_REG` to the desired GPIO output value.
```