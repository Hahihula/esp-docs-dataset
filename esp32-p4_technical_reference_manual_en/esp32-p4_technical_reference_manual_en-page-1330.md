

```markdown
| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | LP_SYSTEM_LP_ADDRHOLE_INT_CLR              | Write 1 to clear LP_ADDRHOLE_INT interrupt. (WT)                            |
| 29  | LP_SYSTEM_IDBUS_ADDRHOLE_INT_CLR           | Write 1 to clear IDBUS_ADDRHOLE_INT interrupt. (WT)                         |
| 28  | LP_SYSTEM_LP_CORE_AHB_TIMEOUT_INT_CLR      | Write 1 to clear LP_CORE_AHB_timeout interrupt. (WT)                        |
| 27  | LP_SYSTEM_LP_CORE_IBUS_TIMEOUT_INT_CLR     | Write 1 to clear LP_CORE_IBUS_timeout interrupt. (WT)                       |
| 26  | LP_SYSTEM_LP_CORE_DBUS_TIMEOUT_INT_CLR     | Write 1 to clear LP_CORE_DBUS_timeout interrupt. (WT)                       |
| 25  | LP_SYSTEM_ETM_TASK_ULP_INT_CLR             | Write 1 to clear ETM_TASK_ULP_INT interrupt. (WT)                           |
| 24  | LP_SYSTEM_SLOW_CLK_TICK_INT_CLR            | Write 1 to clear SLOW_CLK_TICK_INT interrupt. (WT)                          |

Register 20.114. LP_SYSTEM_INT_CLR_REG (0x017C)
```