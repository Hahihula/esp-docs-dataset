

```markdown
Chapter 5 VDMA Controller (VDMA)
GoBack

Contiguous Address

In this scenario, the address for each subsequent block continues from the end of the preceding block. To achieve this contiguity, configure DMAC_CHn_SRC_MULTBLK_TYPE or DMAC_CHn_DST_MULTBLK_TYPE to 0 for the source address or destination address to remain continuous across the blocks.

In the case of multi-block transfer, the values of DMAC_CHn_SRC_MULTBLK_TYPE and DMAC_CHn_DST_MULTBLK_TYPE cannot both be selected as contiguous addresses, meaning they cannot both be configured to 0 at the same time. If both are configured to 0 during a multi-block transfer, then the current block will be considered as the last block.

During a multi-block transfer, if DMAC_CHn_SARO_REG and DMAC_CHn_DARO_REG need to have contiguous addresses between blocks, you can indirectly achieve this functionality using linked-list or shadow-register-based multi-block transfer.

Note:
If you have enabled contiguous-address-based multi-block transfer (i.e., DMAC_CHn_SRC_MULTBLK_TYPE or DMAC_CHn_DST_MULTBLK_TYPE is 0), ensure there are at least two blocks in the DMA transfer. Otherwise, it will result in unpredictable behavior.

Auto Reloading

In this scenario, DMAC_CHn_SARO_REG and DMAC_CHn_DARO_REG are reloaded with their initial values at the end of each block. VDMA does not proceed to the next block transfer until software clears the corresponding channel's block transfer complete interrupt by writing 1 to DMAC_CHn_CLEAR_SRC_TRANSCOMP_INTSTAT and DMAC_CHn_CLEAR_DST_TRANSCOMP_INTSTAT.

Note:
If you have enabled auto-reloading-based multi-block transfer, please ensure there are at least two blocks in the DMA transfer. Otherwise, it will result in unpredictable behavior.

Shadow Register

In this scenario, DMAC_CHn_SARO_REG, DMAC_CHn_DARO_REG, DMAC_CHn_BLOCK_TS, DMAC_CHn_CTL0_REG, and DMAC_CHn_CTL1_REG synchronize with their corresponding shadow registers when each block finishes. The values of the shadow registers are then used for the subsequent block.

Software writes the block configurations to the corresponding shadow registers. VDMA copies the shadow register contents to DMAC_CHn_SARO_REG, DMAC_CHn_DARO_REG, DMAC_CHn_BLOCK_TS, DMAC_CHn_CTL0_REG, and DMAC_CHn_CTL1_REG before starting the subsequent block transfer.

Read operations to the DMAC_CHn_SARO_REG, DMAC_CHn_DARO_REG, DMAC_CHn_BLOCK_TS, DMAC_CHn_CTL0_REG, and DMAC_CHn_CTL1_REG always return the data corresponding to the current block transfer, not the shadow register contents that correspond to the next block.

DMAC_CHn_SHADOWREG_OR_LLI_VALID indicates whether the shadow register contents are valid (1) or not (0). If this bit reads as 0 during a shadow register fetch phase, VDMA discards the shadow register contents and generates a DMAC_CHn_SHADOWREG_OR_LLI_INVALID_ERR_INT interrupt. VDMA waits until the software
```