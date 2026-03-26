

```markdown
| CPU_ICM_H2X_BRESP_ERR_INT | Triggered when a BRESP error occurs in Post Write mode in AHB2AXI |
| HP_CORE1_DBUS_TIMEOUT_INT  | Triggered upon HP CPU1 DBUS timeout                               |
| HP_COREO_DBUS_TIMEOUT_INT  | Triggered upon HP CPU0 DBUS timeout                               |
| HP_CORE1_IBUS_TIMEOUT_INT   | Triggered upon HP CPU1 IBUS timeout                               |
| HP_COREO_IBUS_TIMEOUT_INT   | Triggered upon HP CPU0 IBUS timeout                               |
| HP_CORE1_AHB_TIMEOUT_INT    | Triggered upon HP CPU1 AHB bus timeout                           |
| HP_COREO_AHB_TIMEOUT_INT    | Triggered upon HP CPU0 AHB bus timeout                           |
| ICM_CPU_ADDRHOLE_INT        | Triggered when illegal/unauthorized access occurs in HP CPU and AHB matrix |
| ICM_SYS_ADDRHOLE_INT        | Triggered when illegal/unauthorized access occurs in HP AXI matrix |
| ICM_DLOCK_INT               | Triggered when any AXI transfer in the AXI matrix times out       |

| SLOW_CLK_TICK_INT           | ETM tick event interrupt. The interrupt source is periodically triggered at the frequency of LP_SLOW_CLK when the LP CPU is not sleeping. This event source can be disabled via the LP_CLKRST_ETM_EVENT_TICK_EN. From ULP_TASK_INT_CPU. Ref to 13 Event Task Matrix (ETM) for details |
| LP_CORE_DBUS_TIMEOUT_INT    | Triggered upon LP CPU DBUS timeout                                 |
| LP_CORE_IBUS_TIMEOUT_INT     | Triggered upon LP CPU IBUS timeout                                  |
| LP_CORE_AHB_TIMEOUT_INT      | Triggered upon LP CPU AHB timeout                                   |
| IDBUS_ADDRHOLE_INT           | Triggered when illegal/unauthorized access occurs on LP CPU IBUS or DBUS |
| LP_ADDRHOLE_INT              | Triggered when illegal/unauthorized access occurs in LP AHB matrix   |

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.
```