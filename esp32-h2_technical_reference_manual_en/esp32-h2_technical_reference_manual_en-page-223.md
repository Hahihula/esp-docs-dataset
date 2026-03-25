
```markdown
Note:
There is a range of peripheral output signals (97 ~ 100 in Table 6.12-1) which are not connected to any peripheral, but to the input signals (97 ~ 100) directly.

## 6.5.2 Functional Description

The 99 output signals (signals with a name assigned in the column "Output signal" in Table 6.12-1) can be set to go through GPIO matrix into IO MUX and then to a pin. Figure 6.3-1 illustrates the configuration.

To output peripheral signal Y to a particular GPIO pin X¹, follow the steps below:

1. Configure registers `GPIO_FUNCx_OUT_SEL_CFG_REG` and `GPIO_ENABLE_REG[x]` corresponding to GPIO pin X in GPIO matrix. Recommended operation: use corresponding W1TS (write 1 to set) and W1TC (write 1 to clear) registers to set or clear `GPIO_ENABLE_REG`.

    * Set the `GPIO_FUNCx_OUT_SEL` field in register `GPIO_FUNCx_OUT_SEL_CFG_REG` to the index of the desired peripheral output signal Y.
    * If the signal should always be enabled as an output, set the `GPIO_FUNCx_OEN_SEL` bit in register `GPIO_FUNCx_OUT_SEL_CFG_REG` and the bit in register `GPIO_ENABLE_W1TS_REG`, corresponding to GPIO pin X. To have the output enable signal decided by internal logic (for example, the SPIQ_oe in column "Output enable signal when `GPIO_FUNCn_OEN_SEL = 0"` in Table 6.12-1), clear the `GPIO_FUNCx_OEN_SEL` bit instead.
    * Set the corresponding bit in register `GPIO_ENABLE_W1TC_REG` to disable the output from the GPIO pin.

2. For an open drain output, set the `GPIO_PINx_PAD_DRIVER` bit in register `GPIO_PINx_REG` corresponding to GPIO pin X.

3. Configure IO MUX register to enable output via GPIO matrix. Set `IO_MUX_GPIOx_REG` corresponding to GPIO pin X as follows:

    * Set the field `IO_MUX_GPIOx_MCU_SEL` to desired IO MUX function corresponding to GPIO pin X. This is Function 1 (GPIO function), numeric value 1, for all pins.
    * Set the `IO_MUX_GPIOx_FUN_DRV` field to the desired value for output strength (0 ~ 3). The higher the drive strength, the more current can be sourced/sunk from the pin.

        - 0: ~5 mA
        - 1: ~10 mA
        - 2: ~20 mA (default)
        - 3: ~40 mA

    * If using open drain mode, set/clear the `IO_MUX_GPIOx_FUN_WPU` and `IO_MUX_GPIOx_FUN_WPD` bits to enable/disable the internal pull-up/pull-down resistors.

Note:
1. The output signal from a single peripheral can be sent to multiple pins simultaneously.
2. The output signal can be inverted by setting `GPIO_FUNCx_OUT_INV_SEL`.
```