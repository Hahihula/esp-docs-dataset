

```markdown
Register 17.3. HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG (0x000C)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 18-15     | HP_SYSTEM_CPU_PERI_TIMEOUT_PROTECT_EN      | Configures whether to enable timeout protection for accessing CPU peripheral registers.<br>0: Disable<br>1: Enable (R/W) |
| 17        | HP_SYSTEM_CPU_PERI_TIMEOUT_INT_CLEAR       | Write 1 to clear the timeout interrupt. (WT)                                 |
| 16-0      | HP_SYSTEM_CPU_PERI_TIMEOUT_THRES           | Configures the timeout threshold for bus access for accessing CPU peripheral register in the number of clock cycles of the clock domain. (R/W) |

Register 17.4. HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR_REG (0x0010)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-0      | HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR            | Represents the address information of abnormal access. (RO)                   |

```
```plaintext
GoBack

HP_SYSTEM_CPU_PERI_TIMEOUT_THRES Configures the timeout threshold for bus access for accessing CPU peripheral register in the number of clock cycles of the clock domain. (R/W)

HP_SYSTEM_CPU_PERI_TIMEOUT_INT_CLEAR Write 1 to clear the timeout interrupt. (WT)

HP_SYSTEM_CPU_PERI_TIMEOUT_PROTECT_EN Configures whether to enable timeout protection for accessing CPU peripheral registers.
0: Disable
1: Enable
(R/W)
```
```plaintext
Register 17.4. HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR_REG (0x0010)

HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR Represents the address information of abnormal access.
(RO)
```