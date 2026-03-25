

```markdown
## Register 9.79. PCR_KM_PD_CTRL_REG (0x0168)

PCR_KM_MEM_FORCE_PU Configures whether or not to force power up Key Manager memory.
- O: Not force power up
- 1: Force power up
(R/W)

PCR_KM_MEM_FORCE_PD Configures whether or not to force power down Key Manager memory.
- O: Not force power down
- 1: Force power down
(R/W)
```

```markdown
## Register 9.80. PCR_TCM_MEM_MONITOR_CONF_REG (0x016C)

PCR_TCM_MEM_MONITOR_CLK_EN Configures whether to enable TCM_MEM_MONITOR_CLK.
- O: Not enable
- 1: Enable
(R/W)

PCR_TCM_MEM_MONITOR_RST_EN Configures whether to reset the memory monitor.
- O: Not reset
- 1: Reset
(R/W)

PCR_TCM_MEM_MONITOR_READY Represents whether or not memory monitor is released from reset.
- O: Not released
- 1: Released
(RO)
```