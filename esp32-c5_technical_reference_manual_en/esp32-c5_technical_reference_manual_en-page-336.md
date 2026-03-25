

```markdown
Register 8.3. GPIO_OUT_W1TS_REG (0x0008)

GPIO_OUT_W1TS Configures whether or not to set the output register GPIO_OUT_REG of GPIO0~GPIO14 and GPIO23~GPIO28.
O: Not set
1: The corresponding bit in GPIO_OUT_REG will be set to 1
Bit[0]~bit[14] and bit[23]~bit[28] are corresponding to GPIO0~GPIO14 and GPIO23~GPIO28.
Recommended operation: use this register to set GPIO_OUT_REG.
(WT)

Register 8.4. GPIO_OUT_W1TC_REG (0x000C)

GPIO_OUT_W1TC Configures whether or not to clear the output register GPIO_OUT_REG of GPIO0~GPIO14 and GPIO23~GPIO28 output.
O: Not clear
1: The corresponding bit in GPIO_OUT_REG will be cleared.
Bit[0]~bit[14] and bit[23]~bit[28] are corresponding to GPIO0~GPIO14 and GPIO23~GPIO28.
Recommended operation: use this register to clear GPIO_OUT_REG.
(WT)
```