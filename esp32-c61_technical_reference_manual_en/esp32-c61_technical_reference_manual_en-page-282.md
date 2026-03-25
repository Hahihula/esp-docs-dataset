

```markdown
Register 6.5. GPIO_ENABLE_REG (0x0034)

| Bit | Description |
|-----|-------------|
| 31  | `GPIO_ENABLE_DATA` Configures whether or not to enable the output of GPIO0~GPIO13 and GPIO22~GPIO29.<br>O: Not enable<br>1: Enable<br>Bit[0]~bit[13] and bit[22]~bit[29] are corresponding to GPIO0~GPIO13 and GPIO22~GPIO29.<br>(R/W/WTC) |

Register 6.6. GPIO_ENABLE_W1TS_REG (0x0038)

| Bit | Description |
|-----|-------------|
| 31  | `GPIO_ENABLE_W1TS` Configures whether or not to set the output enable register `GPIO_ENABLE_REG` of GPIO0~GPIO13 and GPIO22~GPIO29.<br>O: Not set<br>1: The corresponding bit in `GPIO_ENABLE_REG` will be set to 1<br>Bit[0]~bit[13] and bit[22]~bit[29] are corresponding to GPIO0~GPIO13 and GPIO22~GPIO29.<br>Recommended operation: use this register to set `GPIO_ENABLE_REG`. (WT) |
```