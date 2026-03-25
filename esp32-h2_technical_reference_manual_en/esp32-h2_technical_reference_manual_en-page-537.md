

```markdown
Register 16.3. HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG (0x000C)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-18     | (reserved)                                |                                                                             |
| 17        | HP_SYSTEM_CPU_PERI_TIMEOUT_PROTECT_EN      | Configures whether to enable timeout protection for accessing CPU peripheral registers. O: Disable, 1: Enable (R/W) |
| 16        | HP_SYSTEM_CPU_PERI_TIMEOUT_INT_CLEAR       | Write 1 to clear timeout interrupt. (WT)                                    |
| 15-0      | HP_SYSTEM_CPU_PERI_TIMEOUT_THRES          | Configures the timeout threshold for bus access for accessing CPU peripheral register in the number of clock cycles of the clock domain. (R/W) |

Register 16.4. HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR_REG (0x0010)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-0      | HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR           | Represents the address information of abnormal access. (RO)                   |
```