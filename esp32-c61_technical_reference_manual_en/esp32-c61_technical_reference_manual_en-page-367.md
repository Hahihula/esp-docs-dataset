

```markdown
Register 742. PCR_TCM_MEM_MONITOR_CONF_REG (0x00C8)
```

| Bit Field | Description |
|-----------|-------------|
| 31-0      | (reserved) |

```markdown
PCR_TCM_MEM_MONITOR_CLK_EN Configures whether or not to enable TCM_MEM_MONITOR clock.
O: Not enable
1: Enable
(R/W)

PCR_TCM_MEM_MONITOR_RST_EN Configures whether or not to reset TCM_MEM_MONITOR.
O: Not reset
1: Reset
(R/W)

PCR_TCM_MEM_MONITOR_READY Represents whether or not TCM_MEM_MONITOR is released from reset.
O: Not released
1: Released
(RO)
```