

```markdown
Register 19.7. PMS_DMA_AHB_PDMA_ADC_R_PMS_REG (0x0128)

PMS_DMA_AHB_PDMA_ADC_R_PMS

31                                 0
+-----------------------------------------------+
|               oxffffffff                | Reset
+-----------------------------------------------+

PMS_DMA_AHB_PDMA_ADC_R_PMS Configures GDMA-AHB permission to read 32 address ranges requested by ADC. Bit 0 corresponds to region0, and so on.

O: Disable read permission.
1: Enable read permission.
(R/W)
```

```markdown
Register 19.8. PMS_DMA_AHB_PDMA_ADC_W_PMS_REG (0x012C)

PMS_DMA_AHB_PDMA_ADC_W_PMS

31                                 0
+-----------------------------------------------+
|               oxffffffff                | Reset
+-----------------------------------------------+

PMS_DMA_AHB_PDMA_ADC_W_PMS Configures GDMA-AHB permission to write 32 address ranges requested by ADC. Bit 0 corresponds to region0, and so on.

O: Disable write permission.
1: Enable write permission.
(R/W)
```