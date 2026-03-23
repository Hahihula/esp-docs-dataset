

```markdown
Register 5.6. GPIO_ENABLE_W1TS_REG (0x0024)

| 31 | 26 | 25 | [reserved] | GPIO_ENABLE_W1TS |
|----:|----:|----:|-----------:|------------------|
|    |     |     |            |                 |
| 0x00000      | Reset |

GPIO_ENABLE_W1TS   GPIO 0 ~ 21 output enable set register. Bit0 ~ bit21 are corresponding to GPIO0 ~ 21, and bit22 ~ bit25 are invalid. If the value 1 is written to a bit here, the corresponding bit in GPIO_ENABLE_REG will be set to 1. Recommended operation: use this register to set GPIO_ENABLE_REG. (WT)

Register 5.7. GPIO_ENABLE_W1TC_REG (0x0028)

| 31 | 26 | 25 | [reserved] | GPIO_ENABLE_W1TC |
|----:|----:|----:|-----------:|------------------|
|    |     |     |            |                 |
| 0x00000      | Reset |

GPIO_ENABLE_W1TC   GPIO 0 ~ 21 output enable clear register. Bit0 ~ bit21 are corresponding to GPIO0 ~ 21, and bit22 ~ bit25 are invalid. If the value 1 is written to a bit here, the corresponding bit in GPIO_ENABLE_REG will be cleared. Recommended operation: use this register to clear GPIO_ENABLE_REG. (WT)

Register 5.8. GPIO_STRAP_REG (0x0038)

| 31 | [reserved] | 16 | 15 | GPIO_STRAPPING |
|----:|------------:|----:|----:|---------------|
|    |             |     |     |               |
| 0x00      | Reset |

GPIO_STRAPPING   GPIO strapping values. (RO)
• bit 0: GPIO2
• bit 2: GPIO8
• bit 3: GPIO9
```