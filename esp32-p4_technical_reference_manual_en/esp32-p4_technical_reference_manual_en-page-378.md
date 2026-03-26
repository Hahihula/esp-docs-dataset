

```markdown
Register 5.12. DMAC_CHn_CTL1_REG (n: 1-4) (0x0100*n + 0x001C)

Continued from the previous page...

DMAC_CHn_DST_STAT_EN Configures whether to enable fetch of destination status.
This logic enables the fetch of the status from the destination peripheral of channel n pointed to by DMAC_CHn_DSTATARO. The value is subsequently stored in DMAC_CHn_DSTAT. At the end of each block transfer, the status value is written back to the DMAC_CHn_DSTAT register of the linked list, if either source or destination peripheral uses linked-list-based multi-block transfer.
0: Do not fetch destination status
1: Fetch destination status and store the value in DMAC_CHn_DSTAT
(R/W)

DMAC_CHn_IOC_BLKTFR Configures whether to enable the interrupt on completion of multi-block transfer based on shadow register or linked list.

Note: If the source and destination uses contiguous-address or auto-reloading-based multi-block transfer, this field cannot be modified on a block by block basis. In addition, the programmed value before enabling the channel will be used for all the blocks in DMA transfer.
0: Disable DMAC_CHn_BLOCK_TFR_DONE_INTSTAT
1: Enable DMAC_CHn_BLOCK_TFR_DONE_INTSTAT, valid when DMAC_CHn_ENABLE_BLOCK_TFR_DONE_INTSTAT is 1. To output a DMAC_CHn_BLOCK_TFR_DONE_INT interrupt, set DMAC_CHn_ENABLE_BLOCK_TFR_DONE_INTSIGNAL to 1.
(R/W)

DMAC_CHn_SHADOWREG_OR_LLI_LAST Configures whether the shadow register or linked list item is the last one.
0: Not the last one
1: The last one
(R/W)

DMAC_CHn_SHADOWREG_OR_LLI_VALID Configures whether the contents of shadow register or the linked list item are valid.
0: Invalid
1: Valid
(R/W)
```