

```markdown
Register 6.5. GPIO_ENABLE_W1TS_REG (0x0024)

31                                 0
+---------------------------------------------------------------+
|                   0x000000                 |Reset|
+---------------------------------------------------------------+

GPIO_ENABLE_W1TS   Configures whether or not to set the output enable register GPIO_ENABLE_REG of GPIO0 ~ GPIO27.
O: Not set
1: The corresponding bit in GPIO_ENABLE_REG will be set to 1
Bit0 ~ bit27 are corresponding to GPIO0 ~ GPIO27. Bit28 ~ bit31 are invalid. Recommended operation: use this register to set GPIO_ENABLE_REG.
(WT)

Register 6.6. GPIO_ENABLE_W1TC_REG (0x0028)

31                                 0
+---------------------------------------------------------------+
|                   0x000000                 |Reset|
+---------------------------------------------------------------+

GPIO_ENABLE_W1TC   Configures whether or not to clear the output enable register GPIO_ENABLE_REG of GPIO0 ~ GPIO27.
O: Not clear
1: The corresponding bit in GPIO_ENABLE_REG will be cleared
Bit0 ~ bit27 are corresponding to GPIO0 ~ GPIO27. Bit28 ~ bit31 are invalid. Recommended operation: use this register to clear GPIO_ENABLE_REG.
(WT)
```