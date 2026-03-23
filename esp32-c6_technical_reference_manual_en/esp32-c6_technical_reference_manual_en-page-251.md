

```markdown
2. For an open drain output, set the GPIO_PINx_PAD_DRIVER bit in register GPIO_PINx_REG corresponding to GPIO pin X.

3. Configure IO MUX register to enable output via GPIO matrix. Set IO_MUX_GPIOx_REG corresponding to GPIO pin X as follows:

- Set the field IO_MUX_GPIOx_MCU_SEL to desired IO MUX function corresponding to GPIO pin X.
  This is Function 1 (GPIO function), numeric value 1, for all pins.

- Set the IO_MUX_GPIOx_FUN_DRV field to the desired value for output strength (0 ~ 3). The higher the drive strength, the more current can be sourced/sunk from the pin.
  - 0: ~5 mA
  - 1: ~10 mA
  - 2: ~20 mA (default)
  - 3: ~40 mA

- If using open drain mode, set/clear the IO_MUX_GPIOx_FUN_WPU and IO_MUX_GPIOx_FUN_WPD bits to enable/disable the internal pull-up/pull-down resistors.

Note:
1. The output signal from a single peripheral can be sent to multiple pins simultaneously.
2. The output signal can be inverted by setting GPIO_FUNCx_OUT_INV_SEL.

7.5.3 Simple GPIO Output

GPIO matrix can also be used for simple GPIO output. For this case, one GPIO pin can be configured to directly output the desired value, without routing any peripheral output to this pin. This can be done as below:

- Set GPIO matrix GPIO_FUNCn_OUT_SEL with a special peripheral index 128 (0x80);
- Set the corresponding bit in GPIO_OUT_REG register to the desired GPIO output value.

Note:
- GPIO_OUT_REG[0] ~ GPIO_OUT_REG[30] correspond to GPIO0 ~ GPIO30 respectively. GPIO_OUT_REG[31] is invalid.
- Recommended operation: use GPIO_OUT_W1TS/GPIO_OUT_W1TC to set or clear the register GPIO_OUT_REG.

7.5.4 Sigma Delta Modulated Output (SDM)

7.5.4.1 Functional Description

Four out of the 93 peripheral output signals (index: 83 ~ 86 in Table 7.11-1 support 1-bit second-order sigma delta modulation. By default the output is enabled for these four channels. This Sigma Delta modulator can also output PDM (pulse density modulation) signal with configurable duty cycle. The transfer function is:
```