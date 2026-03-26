

```markdown
CHn_STATUS[21:0] corresponds to DMAC_CHn_CMPLTD_BLK_TFR_SIZE, and CHn_STATUS[46:32] corresponds to DMAC_CHn_DATA_LEFT_IN_FIFO[14:0].

Suspension of Transfers Between Blocks

At the end of every block transfer, a block transfer completion interrupt DMAC_CHn_BLOCK_TFR_DONE_INT is generated if:

- Global interrupt is enabled (DMAC_INT_EN = 1)
- The channel block transfer completion interrupt is enabled
  (DMAC_CHn_ENABLE_BLOCK_TFR_DONE_INTSTAT = 1,
   DMAC_CHn_ENABLE_BLOCK_TFR_DONE_INTSIGNAL = 1, DMAC_CHn_IOC_BLKTFR = 1)

For contiguous-address and auto-reloading-based multi-block transfers (neither source nor destination peripheral uses shadow-register or linked-list-based multi-block transfers), the DMA transfer automatically stalls after the DMAC_CHn_BLOCK_TFR_DONE_INT interrupt is generated. VDMA does not proceed to the next block transfer until software writes 1 to DMAC_CHn_CLEAR_BLOCK_TFR_DONE_INTSTAT to clear the interrupt.

Channel suspension between blocks ensures that the block transfer done ISR (Interrupt Service Routine) of the next-to-last block is serviced before the final block transfer starts. This ensures that the ISR has cleared DMAC_CHn_SRC_MULTBLK_TYPE and DMAC_CHn_DST_MULTBLK_TYPE before the final block transfer is completed.

End of Multi-Block Transfers

If either source or destination peripheral uses shadow-register or linked-list-based multi-block transfers, then DMAC_CHn_SHADOWREG_OR_LLI_LAST indicates whether the current block is the last in the transfer. If this bit is 1, VDMA recognizes that the current block is the final block in the transfer and completes the DMA transfer operation at the end of the current block transfer.

For contiguous-address and auto-reloading-based multi-block transfers (when neither source nor destination peripheral uses shadow-register or linked-list-based multi-block transfers), if the corresponding multi-block type selection fields DMAC_CHn_SRC_MULTBLK_TYPE and/or DMAC_CHn_DST_MULTBLK_TYPE are 0 at the end of a block transfer, VDMA understands that the previous block was the final block in the transfer and completes the DMA transfer operation.

5.5.5 Flow Controller

The flow controller determines the length of the DMA block transfer. The flow controller can be VDMA, the source peripheral, or the destination peripheral; memory cannot serve as a flow controller.

If the block length is known before enabling the channel, configure VDMA as the flow controller. If the block length is unknown before enabling the channel, use the source or destination peripheral as the flow controller to determine when to terminate the DMA block transfer.

5.5.6 Channel Suspend and Resume

Software can suspend and resume a channel during DMA transfer. To suspend a channel during DMA transfer:
```