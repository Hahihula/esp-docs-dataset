

```markdown
Register 6.7. GPIO_ENABLE_W1TC_REG (0x003C)

GPIO_ENABLE_W1TC Configures whether or not to clear the output enable register GPIO_ENABLE_REG of GPIO0~GPIO13 and GPIO22~GPIO29.

O: Not clear
1: The corresponding bit in GPIO_ENABLE_REG will be cleared
Bit[0]~bit[13] and bit[22]~bit[29] are corresponding to GPIO0~GPIO13 and GPIO22~GPIO29.
Recommended operation: use this register to clear GPIO_ENABLE_REG.
(WT)

Register 6.8. GPIO_IN_REG (0x0064)

GPIO_IN_DATA_NEXT Represents the input value of GPIO0~GPIO13 and GPIO22~GPIO29.
Each bit represents a pin input value:
O: Low level
1: High level
Bit[0]~bit[13] and bit[22]~bit[29] are corresponding to GPIO0~GPIO13 and GPIO22~GPIO29.
(RO)
```