

```markdown
- the LP GPIO matrix lacks a Glitch Filter function.
- The control and status registers must use LP GPIO related registers. See Section 9.19.4 and Section 9.19.5.

Note:
It is possible to have a LP peripheral read a constantly low or constantly high input value without connecting this input to a pin. This can be done by selecting a special `LP_GPIO_SIGy_IN_SEL` input, instead of a GPIO number:

- When `LP_GPIO_SIGy_IN_SEL` is set to 16, input signal is always 0.
- When `LP_GPIO_SIGy_IN_SEL` is set to 24, input signal is always 1.

## 9.5 Peripheral Output via GPIO Matrix

### 9.5.1 Overview

To output a signal from a peripheral via GPIO matrix,

- configure the HP GPIO matrix to route HP peripheral output signals (only signals with a name assigned in the column “Output signal” in Table 9.12-1) to one of the 55 GPIOs (0 ~ 54).
- Or configure the LP GPIO matrix to route LP peripherals (only signals with a name assigned in the column “Output signal” in Table 9.13-1) to one of the 16 LP GPIOs (0 ~ 15).
- The output signal is routed from the peripheral into GPIO matrix and then into IO MUX. IO MUX must be configured to set the chosen pin to GPIO function. This enables the GPIO output signal to be connected to the pin.

Note:
There is a range of peripheral output signals (250 ~ 255 in Table 9.12-1) which are not connected to any peripheral, but to the input signals (250 ~ 255) directly.

### 9.5.2 Simple GPIO Output

GPIO matrix can also be used for simple GPIO output. For this case, one GPIO pin can be configured to directly output the desired value, without routing any peripheral output to this pin.

Follow the steps below to configure HP GPIO matrix for simple GPIO output:

- Set `GPIO_FUNCx_OUT_SEL` with a special peripheral index 256 (0x100).
- Configure the corresponding bit in `GPIO_OUT_REG/GPIO_OUT1_REG` to the desired GPIO output value.

Note:
- `GPIO_OUT_REG[0] ~ GPIO_OUT_REG[31]` correspond to GPIO0 ~ GPIO31, and `GPIO_OUT1_REG[0] ~ GPIO_OUT1_REG[22]` to GPIO32 ~ GPIO54.
- Recommended operation: use `GPIO_OUT/OUT1_W1TS` and `GPIO_OUT/OUT1_W1TC` to set or clear `GPIO_OUT/OUT1_REG`.
```