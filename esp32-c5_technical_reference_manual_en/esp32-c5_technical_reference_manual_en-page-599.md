

```markdown
Chapter 12 Event Task Matrix (ETM)

Register 12.28. SOC_ETM_TASK_ST4_CLR_REG (0x01F4)

Continued from the previous page...

SOC_ETM_GDMA_TASK_OUT_START_CH2_ST_CLR Configures whether or not to clear GDMA_TASK_OUT_START_CH2 trigger status.
O: Invalid. No effect
1: Clear
(WT)

SOC_ETM_PMU_TASK_SLEEP_REQ_ST_CLR Configures whether or not to clear PMU_TASK_SLEEP_REQ trigger status.
O: Invalid. No effect
1: Clear
(WT)

Register 12.29. SOC_ETM_CLK_EN_REG (0x01F8)

SOC_ETM_CLK_EN Configures whether or not to open register clock gate.
O: Open the clock gate only when application writes registers
1: Force open the clock gate for register
(R/W)

Register 12.30. SOC_ETM_DATE_REG (0x01FC)

SOC_ETM_DATE Version control register. (R/W)
```