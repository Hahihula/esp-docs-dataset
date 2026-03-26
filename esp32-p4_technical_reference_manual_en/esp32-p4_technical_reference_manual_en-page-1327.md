

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.111. LP_SYSTEM_INT_RAW_REG (0x0170)
```

```plaintext
31          7   6   5   4   3   2   1   0
+-----------------------------------------------+
| LP_SYSTEM_SLOW_CLK_TICK_INT_RAW | LP_SYSTEM_ETM_TASK_ULP_INT_RAW |
| LP_SYSTEM_LP_CORE_DBUS_TIMEOUT_INT_RAW | LP_SYSTEM_LP_CORE_IBUS_TIMEOUT_INT_RAW |
| LP_SYSTEM_LP_CORE_AHB_TIMEOUT_INT_RAW | LP_SYSTEM_IDBUS_ADDRHOLE_INT_RAW |
| LP_SYSTEM_LP_ADDRHOLE_INT_RAW | Reset                                     |
+-----------------------------------------------+
(reserved)
```

```markdown
LP_SYSTEM_LP_ADDRHOLE_INT_RAW The raw interrupt status of LP_ADDRHOLE_INT.
(R/SS/WTC)

LP_SYSTEM_IDBUS_ADDRHOLE_INT_RAW The raw interrupt status of IDBUS_ADDRHOLE_INT.
(R/SS/WTC)

LP_SYSTEM_LP_CORE_AHB_TIMEOUT_INT_RAW The raw interrupt status of
LP_CORE_AHB_TIMEOUT_INT. (R/SS/WTC)

LP_SYSTEM_LP_CORE_IBUS_TIMEOUT_INT_RAW The raw interrupt status of
LP_CORE_IBUS_TIMEOUT_INT. (R/SS/WTC)

LP_SYSTEM_LP_CORE_DBUS_TIMEOUT_INT_RAW The raw interrupt status of
LP_CORE_DBUS_TIMEOUT_INT. (R/SS/WTC)

LP_SYSTEM_ETM_TASK_ULP_INT_RAW The raw interrupt status of ETM_TASK_ULP_INT.
(R/SS/WTC)

LP_SYSTEM_SLOW_CLK_TICK_INT_RAW The raw interrupt status of SLOW_CLK_TICK_INT.
(R/SS/WTC)
```