

```markdown
Register 19.29. PMS_DMA_AXI_PDMA_AES_R_PMS_REG (0x0194)

31                                 0
+------------------------------------------------------------------------------+
|                 0xffffff                                                Reset |
+------------------------------------------------------------------------------+

PMS_DMA_AXI_PDMA_AES_R_PMS Configures GDMA-AXI permission to read 32 address ranges requested by AES. Bit 0 corresponds to region0, and so on.
O: Disable read permission.
1: Enable read permission.
(R/W)

Register 19.30. PMS_DMA_AXI_PDMA_AES_W_PMS_REG (0x0198)

31                                 0
+------------------------------------------------------------------------------+
|                 0xffffff                                                Reset |
+------------------------------------------------------------------------------+

PMS_DMA_AXI_PDMA_AES_W_PMS Configures GDMA-AXI permission to write 32 address ranges requested by AES. Bit 0 corresponds to region0, and so on.
O: Disable write permission.
1: Enable write permission.
(R/W)
```