

```markdown
## Register 17.9. LP_PERI_BUS_TIMEOUT_CONF_REG (0x0010)

| Bit Field | Description |
|-----------|-------------|
| LP_PERI_BUS_TIMEOUT_PROTECT_EN | Configures whether to enable timeout protection for accessing LP peripheral registers.<br>0: Disable<br>1: Enable<br>(R/W) |
| LP_PERI_BUS_TIMEOUT_INT_CLEAR | Write 1 to clear timeout interrupt. (WT) |
| LP_PERI_BUS_TIMEOUT_THRES | Configures the timeout threshold for bus access for accessing LP peripheral register, corresponding to the number of clock cycles of the clock domain. (R/W) |

## Register 17.10. LP_PERI_BUS_TIMEOUT_ADDR_REG (0x0014)

| Bit Field | Description |
|-----------|-------------|
| LP_PERI_BUS_TIMEOUT_ADDR | Represents the address information of abnormal access. (RO) |
```