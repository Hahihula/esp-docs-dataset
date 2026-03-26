

```markdown
## 6.9 Registers

The addresses in this section are relative to 2D-DMA base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 6.1. DMA2D_OUT_CONFO_CHn_REG (n: 0-3) (0x0000+0x100*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0 |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | DMA2D_OUT_AUTO_WRBACK_CHn | DMA2D_OUT_MODE_CHn | DMA2D_OUT_EEOF_MODE_CHn | DMA2D_OUT_OWNTER_CHn | DMA2D_OUT_REORDER_EN_CHn | DMA2D_OUT_SDSR_PORT_EN_CHn | DMA2D_OUT_MEM_BURST_LENGTH_CHn | DMA2D_OUT_BLOCK_SIZE_CHn | (reserved) | DMA2D_OUT_ARB_WEIGHT_OPT_DIS_CHn | DMA2D_OUT_CMD_RST_CHn | DMA2D_OUT_ARB_WEIGHT_OPT_DIS_CHn | (reserved) |

DMA2D_OUT_AUTO_WRBACK_CHn Configures whether to enable automatic outlink write-back when all the data in TX FIFO has been transmitted.
- O: Disable
- 1: Enable
(R/W)

DMA2D_OUT_EEOF_MODE_CHn Configures when to generate EOF flag.
- 1: EOF flag for TX channel n is generated when data need to read has been pushed into FIFO of 2DDMA
- 1: EOF flag for TX channel n is generated when data need to read has been popped from FIFO of 2DDMA
(R/W)

DMA2D_OUTDSR_BURST_EN_CHn Configures whether to enable INCR burst transfer for TX channel n reading descriptors.
- O: Disable
- 1: Enable
(R/W)

DMA2D_OUT_ECC_AES_EN_CHn Configures to enable the access to external memory space for ECC and AES (encrypted) via TX channel n.
- O: Disable
- 1: Enable
In this case, the starting address of the space and the corresponding data should be 16-byte aligned.
(R/W)

Continued on the next page...
```