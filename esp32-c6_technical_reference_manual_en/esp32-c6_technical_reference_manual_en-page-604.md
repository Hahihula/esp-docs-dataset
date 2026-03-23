

```markdown
Register 17.10. LP_PERI_BUS_TIMEOUT_CONF_REG (0x0010)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                                 |                                                                             |
| 18-16     | LP_PERI_BUS_TIMEOUT_PROTECT_EN             | Configures whether to enable timeout protection for accessing LP peripheral registers. O: Disable<br>1: Enable (R/W) |
| 15        | LP_PERI_BUS_TIMEOUT_INT_CLEAR              | Configures whether to clear timeout interrupt.<br>0: No effect<br>1: Clear timeout interrupt (WT) |
| 14-0      | LP_PERI_BUS_TIMEOUT_THRES                  | Configures the timeout threshold for bus access for accessing LP peripheral register, corresponding to the number of clock cycles of the clock domain. (R/W) |

Register 17.11. LP_PERI_BUS_TIMEOUT_ADDR_REG (0x0014)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31        | LP_PERI_BUS_TIMEOUT_ADDR                   | Represents the address information of abnormal access. (RO)                    |

LP_PERI_BUS_TIMEOUT_THRES Configures the timeout threshold for bus access for accessing LP peripheral register, corresponding to the number of clock cycles of the clock domain. (R/W)

LP_PERI_BUS_TIMEOUT_INT_CLEAR Configures whether to clear timeout interrupt.
0: No effect
1: Clear timeout interrupt
(WT)

LP_PERI_BUS_TIMEOUT_PROTECT_EN Configures whether to enable timeout protection for accessing LP peripheral registers.
0: Disable
1: Enable
(R/W)
```