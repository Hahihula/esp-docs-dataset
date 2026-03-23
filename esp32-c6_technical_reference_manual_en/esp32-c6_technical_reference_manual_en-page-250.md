

```markdown
GPIO pin.

To implement simple GPIO input, follow the steps below:

*   Set `IO_MUX_GPIOx_FUNC_EN` in register `IO_MUX_GPIOx_REG`, to enable pin input.
*   Read the GPIO input from `GPIO_IN_REG[x]`.

## 7.5 Peripheral Output via GPIO Matrix

### 7.5.1 Overview

To output a signal from a peripheral via GPIO matrix, the matrix is configured to route peripheral output signals (only signals with a name assigned in the column “Output signal” in Table 7.11-1) to one of the 31 GPIOs (0 ~ 30). Note:

*   For chip variants without an-in-package flash, output signals can be mapped to 30 GPIO pins, i.e., GPIO0 ~ GPIO13, GPIO15 ~ GPIO30.
*   For chip variants with an in-package flash, output signals can only be mapped to 22 GPIO pins, i.e., GPIO0 ~ GPIO9, GPIO12 ~ GPIO23.

The output signal is routed from the peripheral into GPIO matrix and then into IO MUX. IO MUX must be configured to set the chosen pin to GPIO function. This enables the GPIO output signal to be connected to the pin.

**Note:**
There is a range of peripheral output signals (97 ~ 100 in Table 7.11-1) which are not connected to any peripheral, but to the input signals (97 ~ 100) directly.

### 7.5.2 Functional Description

The 93 output signals (signals with a name assigned in the column “Output signal” in Table 7.11-1) can be set to go through GPIO matrix into IO MUX and then to a pin. Figure 7.3-1 illustrates the configuration.

To output peripheral signal `Y` to a particular GPIO pin `X`, follow the steps below:

1.  Configure registers `GPIO_FUNCx_OUT_SEL_CFG_REG` and `GPIO_ENABLE_REG[X]` corresponding to GPIO pin `X` in GPIO matrix. Recommended operation: use corresponding W1TS (write 1 to set) and W1TC (write 1 to clear) registers to set or clear `GPIO_ENABLE_REG`.

    *   Set the `GPIO_FUNCx_OUT_SEL` field in register `GPIO_FUNCx_OUT_SEL_CFG_REG` to the index of the desired peripheral output signal `Y`.
    *   If the signal should always be enabled as an output, set the `GPIO_FUNCx_OEN_SEL` bit in register `GPIO_FUNCx_OUT_SEL_CFG_REG` and the bit in register `GPIO_ENABLE_W1TS_REG`, corresponding to GPIO pin `X`. To have the output enable signal decided by internal logic (for example, the SPIQ_oen in column “Output enable signal when `GPIO_FUNCn_OEN_SEL = '0'` in Table 7.11-1), clear the `GPIO_FUNCx_OEN_SEL` bit instead.
    *   Set the corresponding bit in register `GPIO_ENABLE_W1TC_REG` to disable the output from the GPIO pin.
```