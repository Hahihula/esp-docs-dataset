

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC)

Register 52.1. DMABUSMODE_REG (0x1000)

Continued from the previous page...

PBLX8_MODE Configures whether to multiply the PBL (programmable burst length) value by 8.
O: Disable
1: The programmed PBL value (PROG_BURST_LEN and RX_DMA_PBL) is multiplied by 8. Therefore, the DMA transfers the data in 8, 16, 32, 64, 128, and 256 beats depending on the PBL value.
(R/W)

USE_SEP_PBL Configures whether to use separate PBL.
O: PROG_BURST_LEN is applicable only for TX DMA, and RX DMA uses RX_DMA_PBL.
1: PROG_BURST_LEN is applicable for both TX and RX DMA.
(R/W)

RX_DMA_PBL Configure the maximum number of beats to be transferred in one RX DMA transaction, namely the maximum value that is used in a single block Read or Write.
Value range: 1, 2, 4, 8, 16 and 32. Any other value results in undefined behavior.
Valid only when USE_SEP_PBL is set.
(R/W)

FIXED_BURST Configures whether the AHB Master interface performs fixed burst transfers.
O: The AHB interface uses SINGLE and INCR burst transfer operations.
1: The AHB interface uses only SINGLE, INCR4, INCR8, or INCR16 during start of the normal burst transfers.
(R/W)

PRI_RATIO Configures the priority ratio in the weighted round-robin arbitration between the RX DMA and TX DMA.
O: 1:1
1: 2:0
2: 3:1
3: 4:1
Valid only when DMA_ARB_SCH is 0. (R/W)

PROG_BURST_LEN Configures the maximum number of beats to be transferred in one DMA transaction.
If the number of beats to be transferred is more than 32, then perform the following steps:
1. Set the PBLx8 mode with PBLX8_MODE
2. Set the PBL with PROG_BURST_LEN
(R/W)

ALT_DESC_SIZE Configures whether to increase the descriptor size to 32 bytes.
O: Keep 16 bytes
1: Increase to 32 bytes
(R/W)

DESC_SKIP_LEN Configures the number of Word, Dword, or Lword (depending on the 32-bit, 64-bit, or 128-bit bus) to skip between two unchained descriptors.
The address skipping starts from the end of the current descriptor to the start of next descriptor.
When this field is 0, the descriptor table is taken as contiguous by the DMA in Ring mode.

Continued on the next page...
```