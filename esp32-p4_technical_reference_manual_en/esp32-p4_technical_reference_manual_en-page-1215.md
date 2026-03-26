

```markdown
Chapter 19 Permission Control (PMS)

Register 19.72. PMS_LP_MM_PMS_REG1_REG (0x0030)
```

Continued from the previous page...

```markdown
PMS_LP_MM_HP_BITSCRAMBLER_ALLOW Configures whether the LP CPU in machine mode has permission to access HP bit scrambler.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_AXI_ICM_ALLOW Configures whether the LP CPU in machine mode has permission to access HP AXI ICM.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_PERI_PMS_ALLOW Configures whether the LP CPU in machine mode has permission to access HP_PERI_PMS_REG.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_LP2HP_PERI_PMS_ALLOW Configures whether the LP CPU in machine mode has permission to access LP2HP_PERI_PMS_REG.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_DMA_PMS_ALLOW Configures whether the LP CPU in machine mode has permission to access HP_DMA_PMS_REG.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_H264_DMA2D_ALLOW Configures whether the LP CPU in machine mode has permission to access 2D-DMA.
O: Not allowed
1: Allowed
(R/W)
```