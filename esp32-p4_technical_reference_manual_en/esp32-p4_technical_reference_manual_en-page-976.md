

```markdown
Register 13.38. SOC_ETM_TASK_ST6_CLR_REG (0x021C)

Continued from the previous page...

SOC_ETM_DMA2D_TASK_OUT_DSCR_READY_CHO_ST_CLR   Configures whether to clear DMA2D_TASK_OUT_DSCR_READY_CHO.
O: Invalid. No effect
1: Clear
(WT)

SOC_ETM_DMA2D_TASK_OUT_DSCR_READY_CH1_ST_CLR   Configures whether to clear DMA2D_TASK_OUT_DSCR_READY_CH1.
O: Invalid. No effect
1: Clear
(WT)

SOC_ETM_DMA2D_TASK_OUT_DSCR_READY_CH2_ST_CLR   Configures whether to clear DMA2D_TASK_OUT_DSCR_READY_CH2.
O: Invalid. No effect
1: Clear
(WT)

Register 13.39. SOC_ETM_CLK_EN_REG (0x0220)
```
```markdown
(reserved) SOCEETMCLKEN

31 | 0
-----------------------------------------------
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 Reset

SOC_ETM_CLK_EN   Configures register clock gating.
O: Support clock only when application writes registers
1: Force on clock gating for registers
(R/W)
```