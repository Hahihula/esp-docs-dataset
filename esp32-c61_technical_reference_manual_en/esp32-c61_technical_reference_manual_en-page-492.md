

```markdown
## Register 10.26. SOC_ETM_TASK_ST4_CLR_REG (0x01EC)

SOC_ETM_GDMA_AHB_TASK_OUT_START_CH1_ST_CLR Configures whether or not to clear GDMA_AHB_TASK_OUT_START_CH1 trigger status.
- O: Invalid. No effect
- 1: Clear (WT)

SOC_ETM_PMU_TASK_SLEEP_REQ_ST_CLR Configures whether or not to clear PMU_TASK_SLEEP_REQ trigger status.
- O: Invalid. No effect
- 1: Clear (WT)

## Register 10.27. SOC_ETM_CLK_EN_REG (0x01F0)

SOC_ETM_CLK_EN Configures whether or not to open register clock gate.
- O: Open the clock gate only when application writes registers
- 1: Force open the clock gate for register (R/W)
```