

# 54.13 Registers

The addresses in this section are relative to the SD/MMC Host Controller base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 54.1. SDHOST_CTRL_REG (0x0000)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

**SDHOST_CONTROLLER_RESET** Configures whether to reset the controller. This bit is auto-cleared after controller reset.
- O: No effect
- 1: Reset (R/W)

**SDHOST_FIFO_RESET** Configures whether to reset FIFO. This bit is auto-cleared after FIFO reset.
- O: No effect
- 1: Reset (R/W)

**SDHOST_DMA_RESET** Configures whether to reset DMA interface. This bit is auto-cleared after DMA reset.
- O: No effect
- 1: Reset (R/W)

**SDHOST_INT_ENABLE** Write 1 to enable global interrupt port. (R/W)

**SDHOST_READ_WAIT** Configures whether to send read-wait to SDIO cards.
- O: Clear read wait
- 1: Assert read wait (R/W)

Continued on the next page...