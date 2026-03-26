

```markdown
Register 21.1. SPM_MEM_MONITOR_LOG_SETTING_REG (0x0000)

Continued from the previous page...

SPM_MEM_MONITOR_LOG_CORE_ENA Configures whether to enable HP CPU0 or HP CPU1 bus access logging.
bit[0]: Configures whether to enable HP CPU0 bus access logging.
O: Disable
1: Enable
bit[1]: Configures whether to enable HP CPU1 bus access logging.
O: Disable
1: Enable
(R/W)

Register 21.2. SPM_MEM_MONITOR_LOG_CHECK_DATA_REG (0x0008)
```

```markdown
SPM_MEM_MONITOR_LOG_CHECK_DATA Configures the data to be monitored during bus accessing. (R/W)
```