

```markdown
- DMAC_CHn_SLVIF_WRONCHEN_ERR_INT: Slave interface write on-enabled channel error interrupt
- DMAC_CHn_SLVIF_RD2RWO_ERR_INT: Slave interface read to write-only error interrupt
- DMAC_CHn_SLVIF_WR2RO_ERR_INT: Slave interface write to read-only error interrupt
- DMAC_CHn_SLVIF_DEC_ERR_INT: Slave interface decode error interrupt
- DMAC_CHn_SLVIF_MULTIBLKTYPE_ERR_INT: Slave interface multi-block type error interrupt
- DMAC_CHn_SHADOW_REG_OR_LLI_INVALID_ERR_INT: Shadow register or LLI invalid error interrupt
- DMAC_CHn_LLI_WR_SLV_ERR_INT: LLI write slave error interrupt
- DMAC_CHn_LLI_RD_SLV_ERR_INT: LLI read slave error interrupt
- DMAC_CHn_LLI_WR_DEC_ERR_INT: LLI write decode error interrupt
- DMAC_CHn_LLI_RD_DEC_ERR_INT: LLI read decode error interrupt
- DMAC_CHn_DST_SLV_ERR_INT: Destination slave error interrupt
- DMAC_CHn_SRC_SLV_ERR_INT: Source slave error interrupt
- DMAC_CHn_DST_DEC_ERR_INT: Destination decode error interrupt
- DMAC_CHn_SRC_DEC_ERR_INT: Source decode error interrupt
- DMAC_CHn_DST_TRANSCOMP_INT: Destination transfer completed interrupt
- DMAC_CHn_SRC_TRANSCOMP_INT: Source transfer completed interrupt
- DMAC_CHn_DMA_TFR_DONE_INT: DMA transfer done interrupt
- DMAC_CHn_BLOCK_TFR_DONE_INT: Block transfer done interrupt

## 5.7 Programming Procedures

This section outlines the programming steps for different types of transfers.

### 5.7.1 Common Programming Procedures

The following two steps are common and should be performed before other programming procedures.

1. Set `HP_SYS_CLKRST_GDMA_SYS_CLK_EN` to 1 to enable VDMA bus clock.
2. Configure `TEE_DMA_GDMA_CHn_W_PMS` and `TEE_DMA_GDMA_CHn_R_PMS` to define the access permission of VDMA. For more details please refer to Chapter 19 Permission Control (PMS).

### 5.7.2 Programming Procedures for Shadow-Register-Based Multi-Block Transfer

1. Read `DMAC_CHn_EN` to select an available (unused) channel.
2. Configure `DMAC_CHn_SRC_MULTBLK_TYPE` and/or `DMAC_CHn_DST_MULTBLK_TYPE` to 2 to enable shadow-register-based multi-block transfer for source transfer and/or destination transfer.
```