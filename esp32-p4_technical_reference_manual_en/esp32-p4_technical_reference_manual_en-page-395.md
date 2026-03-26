

```markdown
Register 5.27. DMAC_CHn_STATUS0_REG (n: 1-4) (0x0100*n + 0x0130)

DMAC_CHn_CMPLTD_BLK_TFR_SIZE Indicates the total number of data of width DMAC_CHn_SRC_TR_WIDTH transferred during the previous block transfer.

If any error occurs during DMA transfer, the block transfer might be terminated early. In such case, the value of this field indicates the actual data transferred without error in the current block.

This field is cleared to 0 when the channel is enabled.
(RO)

Register 5.28. DMAC_CHn_STATUS1_REG (n: 1-4) (0x0100*n + 0x0134)

DMAC_CHn_DATA_LEFT_IN_FIFO Indicates the total number of remaining data in the VDMA channel FIFO after completing the current block transfer.

The data width in the channel FIFO is DMAC_CHn_SRC_TR_WIDTH.

For a normal block transfer completion without errors, the value of this field is 0. If any errors occur during DMA transfer, the block transfer may be terminated early; in this case, this field indicates the remaining data in the channel FIFO that cannot be transferred to the target peripheral.

This field will be cleared when the channel is enabled.

If DMAC_CHn_DST_TR_WIDTH > DMAC_CHn_SRC_TR_WIDTH, there may be remaining data in the FIFO that is not enough to form a single transfer of DMAC_CHn_SRC_TR_WIDTH width; in this case, this field will return 0.
(RO)
```