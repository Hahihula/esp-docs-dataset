

```markdown
DMAC_CHn_SHADOWREG_OR_LLI_VALID indicates whether the linked list item fetched from memory is valid (1) or not (0). If the LLI is invalid, VDMA discards the LLI and generates a DMAC_CHn_SHADOWREG_OR_LLI_INVALID_ERR_INT interrupt. This interrupt causes VDMA to halt the corresponding channel and wait until the software writes 1 to DMAC_CHn_BLK_TFR_RESUMEREQ to indicate that the LLI is available. After this, VDMA will attempt to read the LLI again.

Note:
For pre-fetched LLIs, if DMAC_CHn_SHADOWREG_OR_LLI_VALID is 0, then the DMAC_CHn_SHADOWREG_OR_LLI_INVALID_ERR_INTSTAT interrupt will not be generated. VDMA re-attempts to fetch the LLI again after completing the current block transfer and generates a DMAC_CHn_SHADOWREG_OR_LLI_INVALID_ERR_INTSTAT interrupt only if DMAC_CHn_SHADOWREG_OR_LLI_VALID still reads as 0.

The following fields in LLI are prepared by software:

* CHn_SAR: The field definition is the same as DMAC_CHn_SARO_REG
* CHn_DAR: The field definition is the same as DMAC_CHn_DARO_REG
* CHn_BLOCK_TS: The field definition is the same as DMAC_CHn_BLOCK_TS
* CHn_LLPO[31:6]: The field definition is the same as DMAC_CHn_LLPO_REG[31:6]
* CHn_CTLO: The field definition is the same as DMAC_CHn_CTLO_REG
* CHn_CTL1: The field definition is the same as DMAC_CHn_CTL1_REG

If the status write-back option is enabled, VDMA writes back CHn_CTLO, CHn_CTL1, CHn_LLP_STATUS, CHn_SSTAT, and CHn_DSTAT information to the location defined for this field, which is from address [CHn_LLP] + 0x20 to [CHn_LLP] + 0x34. The write-back of CHn_SSTAT and CHn_DSTAT can be independently enabled or disabled by programming DMAC_CHn_SRC_STAT_EN and DMAC_CHn_DST_STAT_EN.

Note:
* If CHn_SSTAT and CHn_DSTAT write-back is not enabled, do not use PSRAM to store LLI.
* DMAC_CHn_SHADOWREG_OR_LLI_VALID will be 0 after the LLI write-back operation.

Figure 5.5-6 shows CHn_LLP_STATUS write-back field of LLI:

| * | Reserved[61:47] | Data Left in Channel FIFO (CHn_Status[46:32]) | Completed Block Transfer Size (CHn_Status[21:0]) |
|---|------------------|-----------------------------------------------|-------------------------------------------------|
| Note: * denotes Status Indication (CHn_IntStatus[1:0]) |

Figure 5.5-6. CHn_LLP_STATUS Write-Back Field of LLI

CHn_LLP_STATUS[63] and CHn_LLP_STATUS[62] indicate DMA_TFR_DONE and BLOCK_TFR_DONE status respectively. These two fields are the last to be updated during LLI write-back. Software should ensure that BLOCK_TFR_DONE bit is set to 1 before using CHn_SSTAT and CHn_DSTAT information. DMA_TFR_DONE and BLOCK_TFR_DONE bits will be set to 1 after transferring the last block.
```