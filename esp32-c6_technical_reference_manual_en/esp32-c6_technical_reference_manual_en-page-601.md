

```markdown
## Register 17.4. HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG (0x000C)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-18     | (reserved)                                 |                                                                             |
| 17        | `HP_SYSTEM_CPU_PERI_TIMEOUT_PROTECT_EN`     | Configures whether or not to enable timeout protection for accessing CPU peripheral registers. <br> O: Disable <br> 1: Enable (R/W) |
| 16        | `HP_SYSTEM_CPU_PERI_TIMEOUT_INT_CLEAR`      | Write 1 to clear timeout interrupt. (WT)                                    |
| 15-12     | `HP_SYSTEM_CPU_PERI_TIMEOUT_THRES`          | Configures the timeout threshold for bus access for accessing CPU peripheral register in the number of clock cycles of the clock domain. (R/W) |

## Register 17.5. HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR_REG (0x0010)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-0      | `HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR`           | Represents the address information of abnormal access. (RO)                   |

```
```plaintext
Register 17.4. HP_SYSTEM_CPU_PERI_TIMEOUT_CONF_REG (0x000C)

[Diagram: Register bit field layout]
31  18  17  16  15
+----+----+----+----+
|    |HP_SYSTEM_CPU_PERI_TIMEOUT_PROTECT_EN|HP_SYSTEM_CPU_PERI_TIMEOUT_INT_CLEAR|HP_SYSTEM_CPU_PERI_TIMEOUT_THRES|
+----+------------------+----------------------+-------------------------------+

0x0fff Reset

HP_SYSTEM_CPU_PERI_TIMEOUT_THRES Configures the timeout threshold for bus access for accessing CPU peripheral register in the number of clock cycles of the clock domain. (R/W)

HP_SYSTEM_CPU_PERI_TIMEOUT_INT_CLEAR Write 1 to clear timeout interrupt. (WT)

HP_SYSTEM_CPU_PERI_TIMEOUT_PROTECT_EN Configures whether or not to enable timeout protection for accessing CPU peripheral registers.
O: Disable
1: Enable
(R/W)

Register 17.5. HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR_REG (0x0010)

[Diagram: Register bit field layout]
31
+------------------------------------------+
|HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR           |
+------------------------------------------+

0x000000 Reset

HP_SYSTEM_CPU_PERI_TIMEOUT_ADDR Represents the address information of abnormal access.
(RO)
```