

```markdown
Chapter 19 Permission Control (PMS)

Register 19.72. PMS_LP_MM_PMS_REG1_REG (0x0030)
```

Continued from the previous page...

```markdown
PMS_LP_MM_HP_JPEG_ALLOW Configures whether the LP CPU in machine mode has permission to access HP JPEG.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_PPA_ALLOW Configures whether the LP CPU in machine mode has permission to access HP PPA.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_DMA2D_ALLOW Configures whether the LP CPU in machine mode has permission to access HP 2D-DMA.
O: Not allowed 1: Allowed
(R/W)

PMS_LP_MM_HP_KEY_MANAGER_ALLOW Configures whether the LP CPU in machine mode has permission to access HP Key Manager.
O: Not allowed 1: Allowed
(R/W)

PMS_LP_MM_HP_AXI_PDMA_ALLOW Configures whether the LP CPU in machine mode has permission to access HP GDMA-AXI.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_FLASH_ALLOW Configures whether the LP CPU in machine mode has permission to access HP flash MSPI controller.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_PSRAM_ALLOW Configures whether the LP CPU in machine mode has permission to access HP PSRAM MSPI controller.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_HP_CRYPTO_ALLOW Configures whether the LP CPU in machine mode has permission to access HP CRYPTO.
O: Not allowed
1: Allowed
(R/W)
```

Continued on the next page...
```