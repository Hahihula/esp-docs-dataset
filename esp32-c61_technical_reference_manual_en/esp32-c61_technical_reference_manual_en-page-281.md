

```markdown
Register 6.3. GPIO_OUT_W1TS_REG (0x0008)

GPIO_OUT_W1TS   Configures whether or not to set the output register GPIO_OUT_REG of GPIO0~GPIO13 and GPIO22~GPIO29.
O: Not set
1: The corresponding bit in GPIO_OUT_REG will be set to 1
Bit[0]~bit[13] and bit[22]~bit[29] are corresponding to GPIO0~GPIO13 and GPIO22~GPIO29.
Recommended operation: use this register to set GPIO_OUT_REG.
(WT)

Register 6.4. GPIO_OUT_W1TC_REG (0x000C)

GPIO_OUT_W1TC   Configures whether or not to clear the output register GPIO_OUT_REG of GPIO0~GPIO13 and GPIO22~GPIO29.
O: Not clear
1: The corresponding bit in GPIO_OUT_REG will be cleared.
Bit[0]~bit[13] and bit[22]~bit[29] are corresponding to GPIO0~GPIO13 and GPIO22~GPIO29.
Recommended operation: use this register to clear GPIO_OUT_REG.
(WT)
```