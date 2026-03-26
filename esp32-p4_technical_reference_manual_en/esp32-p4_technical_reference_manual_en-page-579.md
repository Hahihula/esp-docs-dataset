

```markdown
## 9.20.1 HP GPIO Matrix Registers

The addresses in this section are relative to HP GPIO matrix base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section IX .

### Register 9.1. GPIO_OUT_REG (0x0004)

| Bit | Description |
|-----|-------------|
| 31  | `GPIO_OUT_DATA_ORIG` Configures the output value of GPIO0 ~ GPIO31 output in simple GPIO output mode.<br>0: Low level<br>1: High level<br>The value of bit0 ~ bit31 correspond to the output value of GPIO0 ~ GPIO31 respectively. (R/W/SC/WTC) |

### Register 9.2. GPIO_OUT_W1TS_REG (0x0008)

| Bit | Description |
|-----|-------------|
| 31  | `GPIO_OUT_W1TS` Configures whether or not to set the output register `GPIO_OUT_REG` of GPIO0 ~ GPIO31.<br>0: Not set<br>1: The corresponding bit in `GPIO_OUT_REG` will be set to 1<br>Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31. Recommended operation: use this register to set `GPIO_OUT_REG`. (WT) |
```