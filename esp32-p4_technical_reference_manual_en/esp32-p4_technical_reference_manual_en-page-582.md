

```markdown
Register 9.7. GPIO_ENABLE_REG (0x0020)

GPIO_ENABLE_DATA Configures whether or not to enable the output of GPIO0 ~ GPIO31.
O: Not enable
1: Enable
Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31
(R/W/WTC)

Register 9.8. GPIO_ENABLE_W1TS_REG (0x0024)

GPIO_ENABLE_W1TS Configures whether or not to set the output enable register GPIO_ENABLE_REG of GPIO0 ~ GPIO31.
O: Not set
1: The corresponding bit in GPIO_ENABLE_REG will be set to 1
Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31. Recommended operation: use this register to set GPIO_ENABLE_REG.
(WT)
```