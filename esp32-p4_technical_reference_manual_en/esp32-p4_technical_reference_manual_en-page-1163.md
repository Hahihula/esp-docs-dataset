

```markdown
Register 19.17. PMS_DMA_AHB_PDMA_UHCIO_R_PMS_REG (0x0150)

| 31 | 0 |
|-----|----|
|     |    |

0xffffffff Reset

PMS_DMA_AHB_PDMA_UHCIO_R_PMS Configures GDMA-AHB permission to read 32 address ranges requested by UHCI. Bit 0 corresponds to region0, and so on.
0: Disable read permission.
1: Enable read permission.
(R/W)

Register 19.18. PMS_DMA_AHB_PDMA_UHCIO_W_PMS_REG (0x0154)

| 31 | 0 |
|-----|----|
|     |    |

0xffffffff Reset

PMS_DMA_AHB_PDMA_UHCIO_W_PMS Configures GDMA-AHB permission to write 32 address ranges requested by UHCI. Bit 0 corresponds to region0, and so on.
0: Disable write permission.
1: Enable write permission.
(R/W)
```