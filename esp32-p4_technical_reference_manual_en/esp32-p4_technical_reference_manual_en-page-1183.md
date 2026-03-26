

```markdown
Chapter 19 Permission Control (PMS)

Register 19.57. PMS_DMA_AXI_PDMA_DUMMY_R_PMS_REG (0x021C)

31 | 0
+----+---------+
|    | offffff
+----+---------+
Reset

PMS_DMA_AXI_PDMA_DUMMY_R_PMS Configures GDMA-AXI permission to read 32 address ranges requested by Dummy. Bit 0 corresponds to region0, and so on.
O: Disable read permission.
1: Enable read permission.
(R/W)

Register 19.58. PMS_DMA_AXI_PDMA_DUMMY_W_PMS_REG (0x0220)

31 | 0
+----+---------+
|    | offffff
+----+---------+
Reset

PMS_DMA_AXI_PDMA_DUMMY_W_PMS Configures GDMA-AXI permission to write 32 address ranges requested by Dummy. Bit 0 corresponds to region0, and so on.
O: Disable write permission.
1: Enable write permission.
(R/W)

19.7.2 HP_PERI_PMS_REG

The addresses in this section are relative to the HP_PERI_PMS base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.
```

ESP32-P4 TRM
PRELIMINARY