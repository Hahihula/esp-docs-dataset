

```markdown
writes 1 to DMAC_CHn_BLK_TFR_RESUMEREQ, indicating that the shadow registers are available. After this, VDMA attempts to read the shadow registers again and continues with the next block transfer.

Note:
In a shadow-register-based multi-block transfer, the values in DMAC_CHn_SARO_REG, DMAC_CHn_DARO_REG, DMAC_CHn_BLOCK_TS, DMAC_CHn_CTL0_REG, and DMAC_CHn_CTL1_REG correspond to the current transfer configurations. When software writes to these registers, it is actually writing to the corresponding shadow registers.

Linked List

In this scenario, VDMA retrieves a block descriptor for a specific block from memory to update DMAC_CHn_SARO_REG, DMAC_CHn_DARO_REG, DMAC_CHn_BLOCK_TS, DMAC_CHn_CTL0_REG, and DMAC_CHn_CTL1_REG, and then initiates the block transfer. This process is called LLI (Linked List Item) update. The block chaining feature of VDMA uses the linked list pointer register DMAC_CHn_LOCO to store the address of the next linked list item in memory, thereby achieving seamless continuity of data transfer.

Figure 5.5-5 shows the VDMA linked list item:

31
0

| Field                        | Description                     |
|------------------------------|----------------------------------|
| Reserved                     |                                  |
| Reserved                     |                                  |
| CHn_LLP_STATUS[63:32]        |                                  |
| CHn_LLP_STATUS[31:0]         |                                  |
| Write Back for Chn_DSTAT     |                                  |
| Write Back for Chn_SSTAT     |                                  |
| CHn_CTL1[31:0]               |                                  |
| CHn_CTL0[31:0]               |                                  |
| Reserved                     |                                  |
| CHn_LLOP[31:6]               | Reserved[5:0]                   |
| Reserved                     |                                  |
| CHn_BLOCK_TS[31:0]           |                                  |
| Reserved                     |                                  |
| CHn_DAR[31:0]                |                                  |
| Reserved                     |                                  |
| CHn_SAR[31:0]                |                                  |

Figure 5.5-5. VDMA Linked List Item (Descriptor)

VDMA can dynamically extend linked lists, which means you do not need to pre-create the entire linked list in system memory. To enable this feature, set DMAC_CHn_SHADOWREG_OR_LLI_VALID to 1. If the linked list item is the last one, then also configure DMAC_CHn_SHADOWREG_OR_LLI_LAST to 1.
```