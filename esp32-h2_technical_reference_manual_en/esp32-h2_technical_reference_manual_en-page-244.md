

```markdown
Register 6.3. GPIO_OUT_W1TC_REG (0x000C)

GPIO_OUT_W1TC Configures whether or not to clear the output register GPIO_OUT_REG of GPIO0 ~ GPIO27 output.
O: Not clear
1: The corresponding bit in GPIO_OUT_REG will be cleared.
bit0 ~ bit27 are corresponding to GPIO0 ~ GPIO27. Bit28 ~ bit31 are invalid. Recommended operation: use this register to clear GPIO_OUT_REG.
(WT)

Register 6.4. GPIO_ENABLE_REG (0x0020)

GPIO_ENABLE_DATA Configures whether or not to enable the output of GPIO0 ~ GPIO27.
O: Not enable
1: Enable
Bit0 ~ bit27 are corresponding to GPIO0 ~ GPIO27. Bit28 ~ bit31 are invalid.
(R/W/WTC)
```