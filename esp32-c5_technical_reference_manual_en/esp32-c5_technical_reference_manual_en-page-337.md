

```markdown
Register 8.5. GPIO_ENABLE_REG (0x0034)

| Bit | Field         |
|-----|---------------|
| 31  |               |
|     | 0x000000      |
|     | Reset         |

GPIO_ENABLE_DATA Configures whether or not to enable the output of GPIO0~GPIO14 and GPIO23~GPIO28.
O: Not enable
1: Enable
Bit[0]~bit[14] and bit[23]~bit[28] are corresponding to GPIO0~GPIO14 and GPIO23~GPIO28.
(R/W/WTC)

Register 8.6. GPIO_ENABLE_W1TS_REG (0x0038)

| Bit | Field         |
|-----|---------------|
| 31  |               |
|     | 0x000000      |
|     | Reset         |

GPIO_ENABLE_W1TS Configures whether or not to set the output enable register GPIO_ENABLE_REG of GPIO0~GPIO14 and GPIO23~GPIO28.
O: Not set
1: The corresponding bit in GPIO_ENABLE_REG will be set to 1
Bit[0]~bit[14] and bit[23]~bit[28] are corresponding to GPIO0~GPIO14 and GPIO23~GPIO28.
Recommended operation: use this register to set GPIO_ENABLE_REG.
(WT)
```