

```markdown
## Register 7.4. GPIO_ENABLE_REG (0x0020)

| Bit | Description |
|-----|-------------|
| 31  | `GPIO_ENABLE_DATA` Configures whether or not to enable the output of GPIO0 ~ GPIO30.<br>0: Not enable<br>1: Enable<br>Bit0 ~ bit30 are corresponding to GPIO0 ~ GPIO30. Bit31 is invalid.<br>(R/W/WTC) |

## Register 7.5. GPIO_ENABLE_W1TS_REG (0x0024)

| Bit | Description |
|-----|-------------|
| 31  | `GPIO_ENABLE_W1TS` Configures whether or not to set the output enable register `GPIO_ENABLE_REG` of GPIO0 ~ GPIO30.<br>0: Not set<br>1: The corresponding bit in `GPIO_ENABLE_REG` will be set to 1<br>Bit0 ~ bit30 are corresponding to GPIO0 ~ GPIO30. Bit31 is invalid. Recommended operation:<br>use this register to set `GPIO_ENABLE_REG`. (WT) |
```