

```markdown
Register 7.2. GPIO_OUT_W1TS_REG (0x0008)

31                                 0
+---------------------------------------------------------------+
|                 0x000000               |Reset|
+---------------------------------------------------------------+

GPIO_OUT_W1TS Configures whether or not to set the output register GPIO_OUT_REG of GPIO0 ~ GPIO30.
O: Not set
1: The corresponding bit in GPIO_OUT_REG will be set to 1
Bit0 ~ bit30 are corresponding to GPIO0 ~ GPIO30. Bit31 is invalid. Recommended operation:
use this register to set GPIO_OUT_REG.
(WT)

Register 7.3. GPIO_OUT_W1TC_REG (0x000C)

31                                 0
+---------------------------------------------------------------+
|                 0x000000               |Reset|
+---------------------------------------------------------------+

GPIO_OUT_W1TC Configures whether or not to clear the output register GPIO_OUT_REG of GPIO0 ~ GPIO30 output.
O: Not clear
1: The corresponding bit in GPIO_OUT_REG will be cleared.
Bit0 ~ bit30 are corresponding to GPIO0 ~ GPIO30. Bit31 is invalid. Recommended operation:
use this register to clear GPIO_OUT_REG.
(WT)
```