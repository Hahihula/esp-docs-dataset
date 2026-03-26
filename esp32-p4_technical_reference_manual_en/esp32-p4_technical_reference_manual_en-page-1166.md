

```markdown
Register 19.23. PMS_DMA_AXI_PDMA_GPSPI2_R_PMS_REG (0x017C)

| 31 | 0 |
|-----|----|
| oxffffffff | Reset |

PMS_DMA_AXI_PDMA_GPSPI2_R_PMS Configures GDMA-AXI permission to read 32 address ranges requested by G-SPI2. Bit 0 corresponds to region0, and so on.
0: Disable read permission.
1: Enable read permission.
(R/W)

Register 19.24. PMS_DMA_AXI_PDMA_GPSPI2_W_PMS_REG (0x0180)

| 31 | 0 |
|-----|----|
| oxffffffff | Reset |

PMS_DMA_AXI_PDMA_GPSPI2_W_PMS Configures GDMA-AXI permission to write 32 address ranges requested by G-SPI2. Bit 0 corresponds to region0, and so on.
0: Disable write permission.
1: Enable write permission.
(R/W)
```