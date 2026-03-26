

```markdown
- If VDMA reads `DMAC_CHn_SHADOWREG_OR_LLI_VALID` as 0, it may generate a  
  `DMAC_CHn_SHADOWREG_OR_LLI_INVALID_ERR_INT` interrupt. VDMA waits until software writes 1  
  to `DMAC_CHn_BLK_TFR_RESUMEREQ` to indicate valid LLI availability before re-attempting the LLI  
  read operation.
```

## 5.7.4 Programming Procedures for Single-Block Transfer

1. Read `DMAC_CHn_EN` to choose a free (unused) channel.

2. Configure `DMAC_CHn_SRC_MULTBLK_TYPE` and `DMAC_CHn_DST_MULTBLK_TYPE` to 0 to enable contiguous-address-based single-block transfer.

3. Configure `DMAC_CHn_SARO_REG` and/or `DMAC_CHn_DARO_REG`, `DMAC_CHn_BLOCK_TS`,  
   `DMAC_CHn_CTLO_REG`, and `DMAC_CHn_CTL1_REG` for the block.

4. Set `DMAC_CHn_EN` to 1 to enable the channel.

5. Software waits for the `DMAC_CHn_BLOCK_TFR_DONE_INT` interrupt or polls  
   `DMAC_CHn_BLOCK_TFR_DONE_INTSTAT` until it is 1.
```