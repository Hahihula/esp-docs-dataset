

```markdown
3. Configure `DMAC_CHn_SARO_REG` and/or `DMAC_CHn_DARO_REG`, `DMAC_CHn_BLOCK_TS`,  
   `DMAC_CHn_CTLO_REG`, and `DMAC_CHn_CTL1_REG` for the first block. VDMA loads the configured  
   values to the corresponding shadow registers.

Notice: The `DMAC_CHn_SHADOWREG_OR_LLI_VALID` field in `DMAC_CHn_CTL1_REG` must be the last one to be set to 1.

4. Set `DMAC_CHn_EN` to 1 to enable the corresponding channel.

5. VDMA initiates the DMA block transfer operation based on the configurations.
   - The block transfer might start immediately or after the handshaking request, depending on  
     `DMAC_CHn_TT_FC`. Specifically,
     - When the source is memory, the source transfer starts immediately; when the destination is  
       memory, the destination transfer starts immediately.
     - When the source is a peripheral, obtaining data from the source requires waiting for a  
       handshake with the source. When the destination is a peripheral, writing data to the destination  
       requires waiting for a handshake with the destination.

   - VDMA checks `DMAC_CHn_SHADOWREG_OR_LLI_VALID` and if it is seen as 0, VDMA waits until  
     software writes 1 to `DMAC_CHn_BLK_TFR_RESUMEREQ` to indicate valid shadow registers availability. Then VDMA re-attempts shadow register fetch operation. In this case, VDMA may generate a `DMAC_CHn_SHADOWREG_OR_LLI_INVALID_ERR_INT` interrupt.

   - VDMA checks `DMAC_CHn_SHADOWREG_OR_LLI_VALID` and if it is seen as 1, VDMA copies the  
     shadow register contents to the registers used for executing the DMA block transfer (i.e.,  
     `DMAC_CHn_SARO_REG` and/or `DMAC_CHn_DARO_REG`, `DMAC_CHn_BLOCK_TS`,  
     `DMAC_CHn_CTLO_REG`, and `DMAC_CHn_CTL1_REG`) and clears  
     `DMAC_CHn_SHADOWREG_OR_LLI_VALID`.

     - If VDMA sees `DMAC_CHn_SHADOWREG_OR_LLI_LAST` as 1, it understands that the current block is the final block in the transfer and completes the DMA transfer operation at the end of current block transfer.
     - If VDMA sees `DMAC_CHn_SHADOWREG_OR_LLI_LAST` as 0, it understands that there are one or more blocks to be transferred and checks `DMAC_CHn_SHADOWREG_OR_LLI_VALID` again at the end of current block transfer.

6. Software waits `DMAC_CHn_SHADOWREG_OR_LLI_VALID` to be cleared to 0.

7. Configure `DMAC_CHn_SARO_REG` and/or `DMAC_CHn_DARO_REG`, `DMAC_CHn_BLOCK_TS`,  
   `DMAC_CHn_CTLO_REG`, and `DMAC_CHn_CTL1_REG` for the next block. If the next block is the last block, set `DMAC_CHn_SHADOWREG_OR_LLI_LAST` to 1.

Notice: `DMAC_CHn_SHADOWREG_OR_LLI_VALID` must be the lase to be set to 1.

8. Software waits for a `DMAC_CHn_BLOCK_TFR_DONE_INT` interrupt or polls  
   `DMAC_CHn_BLOCK_TFR_DONE_INTSTAT` until it reads as 1 and goes back to Step 6.

Note:

In cases where a `DMAC_CHn_SHADOWREG_OR_LLI_INVALID_ERR_INT` interrupt is generated, follow the recommended flow to resume transfer:
```