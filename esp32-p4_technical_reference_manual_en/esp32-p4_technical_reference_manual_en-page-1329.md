
```markdown
| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 7   | LP_SYSTEM_SLOW_CLK_TICK_INT_ENA     | Write 1 to enable SLOW_CLK_TICK_INT interrupt. (R/W)                        |
| 6   | LP_SYSTEM_ETM_TASK_ULP_INT_ENA      | Write 1 to enable ETM_TASK_ULP_INT interrupt. (R/W)                         |
| 5   | LP_SYSTEM_LP_CORE_DBUS_TIMEOUT_INT_ENA | Write 1 to enable LP_CORE_DBUS_timeout interrupt. (R/W)                   |
| 4   | LP_SYSTEM_LP_CORE_IBUS_TIMEOUT_INT_ENA | Write 1 to enable LP_CORE_IBUS_timeout interrupt. (R/W)                  |
| 3   | LP_SYSTEM_LP_CORE_AHB_TIMEOUT_INT_ENA | Write 1 to enable LP_CORE_AHB_timeout interrupt. (R/W)                   |
| 2   | LP_SYSTEM_IDBUS_ADDRHOLE_INT_ENA    | Write 1 to enable IDBUS_ADDRHOLE_INT interrupt. (R/W)                      |
| 1   | LP_SYSTEM_LP_ADDRHOLE_INT_ENA       | Write 1 to enable LP_ADDRHOLE_INT interrupt. (R/W)                         |
| 0   | Reset                                |                                                                             |

LP_SYSTEM_LP_ADDRHOLE_INT_ENA    Write 1 to enable LP_ADDRHOLE_INT interrupt. (R/W)
LP_SYSTEM_IDBUS_ADDRHOLE_INT_ENA  Write 1 to enable IDBUS_ADDRHOLE_INT interrupt. (R/W)
LP_SYSTEM_LP_CORE_AHB_TIMEOUT_INT_ENA Write 1 to enable LP_CORE_AHB_timeout interrupt. (R/W)
LP_SYSTEM_LP_CORE_IBUS_TIMEOUT_INT_ENA Write 1 to enable LP_CORE_IBUS_timeout interrupt. (R/W)
LP_SYSTEM_LP_CORE_DBUS_TIMEOUT_INT_ENA Write 1 to enable LP_CORE_DBUS_timeout interrupt. (R/W)
LP_SYSTEM_ETM_TASK_ULP_INT_ENA    Write 1 to enable ETM_TASK_ULP_INT interrupt. (R/W)
LP_SYSTEM_SLOW_CLK_TICK_INT_ENA   Write 1 to enable SLOW_CLK_TICK_INT interrupt. (R/W)
```