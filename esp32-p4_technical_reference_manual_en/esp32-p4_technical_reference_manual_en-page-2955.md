

```markdown
7. Start the BitScrambler by clearing the BITSCRAMBLER_TX_HALT bit in the  
BITSCRAMBLER_TX_CTRL_REG register.

8. Start DMA transaction. Please refer to Chapter 4 GDMA Controller (GDMA-AHB, GDMA-AXI) for more information about DMA subsystem and refer to the peripheral chapter if loopback mode is not used.

9. Wait until DMA transaction is done.

10. Halt the BitScrambler by setting the BITSCRAMBLER_TX_HALT in the BITSCRAMBLER_TX_CTRL_REG register.

11. Wait for halt state. The BitScrambler is halted when the BITSCRAMBLER_TX_IN_IDLE bit in the BITSCRAMBLER_TX_STATE_REG register is set.

12. Reset the FIFO by writing a 1 and then a 0 to the BITSCRAMBLER_TX_FIFO_RST bit in the BITSCRAMBLER_TX_CTRL_REG register.

13. The BitScrambler is ready for a new transaction with the current program and LUT configuration. Simply start from step 7 to do this.
```