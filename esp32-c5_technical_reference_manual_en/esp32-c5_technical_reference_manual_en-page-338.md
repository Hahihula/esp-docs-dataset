

```markdown
Register 8.7. GPIO_ENABLE_W1TC_REG (0x003C)

GPIO_ENABLE_W1TC Configures whether or not to clear the output enable register GPIO_ENABLE_REG of GPIO0~GPIO14 and GPIO23~GPIO28.

O: Not clear
1: The corresponding bit in GPIO_ENABLE_REG will be cleared
Bit[0]~bit[14] and bit[23]~bit[28] are corresponding to GPIO0~GPIO14 and GPIO23~GPIO28.
Recommended operation: use this register to clear GPIO_ENABLE_REG.
(WT)

Register 8.8. GPIO_IN_REG (0x0064)

GPIO_IN_DATA_NEXT Represents the input value of GPIO0~GPIO14 and GPIO23~GPIO28.
Each bit represents a pin input value:
O: Low level
1: High level
Bit[0]~bit[14] and bit[23]~bit[28] are corresponding to GPIO0~GPIO14 and GPIO23~GPIO28.
(RO)
```