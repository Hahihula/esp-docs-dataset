

```markdown
9.5.4 Programming Procedure

9.5.4.1 HP GPIO Matrix

The output signals with a name assigned in the column “Output signal” in Table 9.12-1 can be set to go through the HP GPIO matrix into HP IO MUX and then to a pin. Figure 9.3-1 illustrates the configuration.

To output peripheral signal Y to a particular GPIO pin X, follow the steps below:

1. Configure GPIO_FUNCx_OUT_SEL_CFG_REG and GPIO_ENABLE_REG[x] corresponding to GPIO pin X in HP GPIO matrix. Recommended operation: use corresponding W1TS (write 1 to set) and W1TC (write 1 to clear) registers to set to clear GPIO_ENABLE_REG.

    - Set the GPIO_FUNCx_OUT_SEL field in register GPIO_FUNCx_OUT_SEL_CFG_REG to the index of the desired peripheral output signal Y.
    
    - If the signal should always be enabled as an output, set the GPIO_FUNCx_OE_SEL bit in register GPIO_FUNCx_OUT_SEL_CFG_REG and the bit in register GPIO_ENABLE_W1TS_REG, corresponding to GPIO pin X. To have the output enable signal decided by internal logic (for example, the spi2_dqs_pad_oe in column “Output enable signal when GPIO_FUNCn_OE_SEL = 0” in Table 9.12-1), clear the GPIO_FUNCx_OE_SEL bit instead.
    
    - Set the corresponding bit in register GPIO_ENABLE_W1TC_REG to disable the output from the GPIO pin.

2. For an open drain output, set the GPIO_PINx_PAD_DRIVER bit in register GPIO_PINx_REG corresponding to GPIO pin X.

3. Configure HP IO MUX register to enable output via HP GPIO matrix. Set IO_MUX_GPIOx_REG corresponding to GPIO pin X as follows:

    - Set the field IO_MUX_GPIOx_MCU_SEL to desired HP IO MUX function corresponding to GPIO pin X. This is Function 1 (GPIO function), numeric value 1, for all pins.
    
    - Set the IO_MUX_GPIOx_FUN_DRV field to the desired value for output strength (0 ~ 3). The higher the drive strength, the more current can be sourced/sunk from the pin.
    
    - If using open drain mode, set/clear the IO_MUX_GPIOx_FUN_WPU and IO_MUX_GPIOx_FUN_WPD bits to enable/disable the internal pull-up/pull-down resistors.

4. Enable hysteresis function:

    - GPIO00 ~ GPIO15: set LP_IOMUX_LP_GPIO_HYS[x] (x: 0 ~ 15, corresponding to GPIO00 ~ GPIO15).
    
    - GPIO16 ~ GPIO47: set HP_SYSTEM_GPIO_O_HYS_LOW[x] (x: 0 ~ 31, corresponding to GPIO16 ~ GPIO47).
    
    - GPIO48 ~ GPIO54: set HP_SYSTEM_GPIO_O_HYS_HIGH[x] (x: 0 ~ 6, corresponding to GPIO48 ~ GPIO54).
```