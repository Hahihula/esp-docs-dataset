

```markdown
Note:

Recommended operation: use LP_GPIO_OUT_DATA_W1TS and LP_GPIO_OUT_DATA_W1TC to set or clear LP_GPIO_OUT_REG.
```

## 6.5.3 Programming Procedure

### 6.5.3.1 HP GPIO Matrix

The output signals with a name assigned in the column “Output signal” in Table 6.12-1 can be set to go through the HP GPIO matrix into HP IO MUX and then to a pin. Figure 6.3-1 illustrates the configuration.

To output peripheral signal Y to a particular GPIO pin X, follow the steps below:

1. Configure `GPIO_FUNCx_OUT_SEL_CFG_REG` and `GPIO_ENABLE_REG[x]` corresponding to GPIO pin X in HP GPIO matrix. Recommended operation: use corresponding W1TS (write 1 to set) and W1TC (write 1 to clear) registers to set or clear `GPIO_ENABLE_REG`.

   - Set the `GPIO_FUNCx_OUT_SEL` field in register `GPIO_FUNCx_OUT_SEL_CFG_REG` to the index of the desired peripheral output signal Y.
   
   - If the signal should always be enabled as an output, set the bit `GPIO_FUNCx_OE_SEL` and the corresponding bit in `GPIO_ENABLE_W1TS_REG`. To have the output enable signal decided by internal logic (for example, the FSPIQ_oe in column “Output enable signal when GPIO_FUNCn_OE_SEL = 0” in Table 6.12-1), clear the `GPIO_FUNCx_OE_SEL` bit instead.
   
   - Set the corresponding bit in register `GPIO_ENABLE_W1TC_REG` to disable the output from the GPIO pin.

2. For an open drain output, set the field `GPIO_PINx_PAD_DRIVER`.

3. Configure HP IO MUX register to enable output via HP GPIO matrix. Set `IO_MUX_GPIOx_REG` corresponding to GPIO pin X as follows:

   - Set the field `IO_MUX_GPIOx_MCU_SEL` to desired HP IO MUX function corresponding to GPIO pin X. This is Function 1 (GPIO function), numeric value 1, for all pins.
   
   - Set the `IO_MUX_GPIOx_FUN_DRV` field to the desired value for output strength (0~3). The higher the drive strength, the more current can be sourced/sunk from the pin.
   
   - If using open drain mode, set or clear the `IO_MUX_GPIOx_FUN_WPU` and `IO_MUX_GPIOx_FUN_WPD` bits to enable or disable the internal pull-up and pull-down resistors.

4. Enable hysteresis function:

   - See Section 6.10.

**Note:**

- The output signal from a single peripheral can be sent to multiple pins simultaneously.
- The output signal can be inverted by setting `GPIO_FUNCx_OUT_INV_SEL`.
```