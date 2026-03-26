

```markdown
- Configure `DMAC_CHn_SARO_REG` and/or `DMAC_CHn_DARO_REG`, `DMAC_CHn_BLOCK_TS`, `DMAC_CHn_CTL0_REG`, and `DMAC_CHn_CTL1_REG` for the next block.
- Set `DMAC_CHn_CLEAR_SHADOWREG_OR_LLI_INVALID_ERR_INTSTAT` to 1 to clear the interrupt.
- Set `DMAC_CHn_BLK_TFR_RESUMEREQ` to 1 to request for resuming block transfer.

## 5.7.3 Programming Procedures for Linked-List-Based Multi-Block Transfer

1. Reads `DMAC_CHn_EN` to select an available (unused) channel.

2. Configure `DMAC_CHn_SRC_MULTBLK_TYPE` and/or `DMAC_CHn_DST_MULTBLK_TYPE` to 3 to enable linked-list-based transfer for source transfer and/or destination transfer.

3. Configure `DMAC_CHn_LLPO_REG` to define the base address of the first linked list item and the master interface on which the linked list item is available.

4. Create one or more linked list items in the system memory. You can create the entire linked list item in advance or dynamically extend it using `DMAC_CHn_SHADOWREG_OR_LLI_VALID` and `DMAC_CHn_SHADOWREG_OR_LLI_LAST` fields of the LLI. Follow the steps below to dynamically extend the linked list.

   - During the DMA transfer process, when the linked list is not ready, configure `DMAC_CHn_SHADOWREG_OR_LLI_VALID` in the linked list to 0 and wait until the linked list is prepared. Then set `DMAC_CHn_SHADOWREG_OR_LLI_VALID` to 1 to extend the linked list.
   - When it is time to end the DMA transfer, set `DMAC_CHn_SHADOWREG_OR_LLI_LAST` of the last linked list to 1 to indicate the end of the transfer.

5. Set `DMAC_CHn_EN` to 1 to enable the channel.

**Note:**
You can swap the sequence of Step 4 and Step 5. However, if Step 5 is performed before Step 4, or if the linked list item for the next block transfer is not available in system memory during the multi-block transfer (i.e., `DMAC_CHn_SHADOWREG_OR_LLI_VALID` of the fetched LLI is 0), VDMA may generate a `DMAC_CHn_SHADOWREG_OR_LLI_INVALID_ERR_INT` interrupt.

6. VDMA initiates the DMA block transfer operation based on the configurations. The block transfer might start immediately or after the handshaking request, depending on `DMAC_CHn_TT_FC`. VDMA copies the linked list contents to the registers used for executing the DMA block transfer (i.e., `DMAC_CHn_SARO_REG` and/or `DMAC_CHn_DARO_REG`, `DMAC_CHn_BLOCK_TS`, `DMAC_CHn_CTL0_REG`, and `DMAC_CHn_CTL1_REG`) and initiates the DMA block transfer.

7. During the linked list fetch phase:

   - If VDMA reads `DMAC_CHn_SHADOWREG_OR_LLI_LAST` as 1, it understands that the current block is the final block in the transfer and completes the DMA transfer operation at the end of the current block transfer.
   - If VDMA reads `DMAC_CHn_SHADOWREG_OR_LLI_LAST` as 0, it understands that there are one or more blocks to be transferred and goes to Step 6.
```