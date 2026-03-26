
```markdown
## 52.8 Registers

The addresses in this section are relative to EMAC base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 52.1. DMABUSMODE_REG (0x1000)

| Bit | 31 | 30 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 17 | 16 | 15 | 14 | 13 | 8 | 7 | 6 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (DMAREBUILDINCRBURST) | (reserved) | DMATRANSMITPRIORITY | DMAADDRLIBEA | PBLX8, NOSEP_PBL | USE | RX_DMA_PBL | FIXED_BURST | PRI_RATIO | PROC_BURST_LEN | ALT_DESC_SIZE | DESC_SKIP_LEN | DMA_ARB_SCH | SW_RST |
|     | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x01 | 0 | 0x0 | 0x01 | 0 | 0x00 | 0 | Reset |

DMAREBUILDINCRBURST Configures whether to rebuild INCRx burst.
- O: Not rebuild
- 1: If the AHB master gets an EBT (retry, split, or losing bus grant), the AHB master interface rebuilds the pending beats of any burst transfer initiated with INCRx using INCRx and SINGLE. (R/W)

DMATRANSMITPRIORITY Configures whether the transmit DMA has higher priority than the receive DMA during arbitration.
- O: Lower priority
- 1: Higher priority (R/W)

DMAMIXEDBURST Configures whether to use mixed burst.
- O: Not use
- 1: If the FIXED_BURST bit is 1, the AHB Master interface starts all bursts of length more than 16 with INCR (undefined burst) whereas it reverts to fixed burst transfers (INCRx and SINGLE) for burst length of 16 and less. (R/W)

DMAADDRLIBEA Configures whether bursts are aligned to address.
- O: Not aligned to address
- 1: If the FIXED_BURST bit is 1, the AHB interface generates all bursts aligned to the start address LS bits. If the FIXED_BURST bit is 0, the first burst (accessing the data buffer’s start address) is not aligned, but subsequent bursts are aligned to the address. (R/W)

Continued on the next page...
```