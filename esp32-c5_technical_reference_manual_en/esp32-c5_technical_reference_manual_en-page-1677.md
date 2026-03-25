

```markdown
# 44.6 Programming Procedures

Note that these instructions are written for a BitScrambler with the TX path enabled, either in the memory-to-peripheral path, or memory-to-memory path if in loopback mode. For the peripheral-to-memory path, the RX path is used. Unless otherwise indicated, you can exchange "TX" for "RX" in these instructions to configure the RX path.

1. Attach the BitScrambler to a peripheral by configuring HP_SYSTEM_BITSCRAMBLER_PERI_TX_SEL field in HP_SYSTEM_BITSCRAMBLER_PERI_SEL_REG register. Note that this step is required even in loopback mode.
2. Enable the BitScrambler by setting the BITSCRAMBLER_TX_ENA field in the BITSCRAMBLER_TX_CTRL_REG register. Make sure only one of BITSCRAMBLER_TX_ENA and BITSCRAMBLER_RX_ENA is set at any time.
3. Configure loopback mode if required. If loopback mode is needed, set BITSCRAMBLER_LOOP_MODE in the BITSCRAMBLER_SYS_REG register. Otherwise, clear it.
4. Load program into BitScrambler. For each instruction and each 32-bit word within the instruction, set the BITSCRAMBLER_TX_INST_IDX and BITSCRAMBLER_TX_INST_POS fields in the BITSCRAMBLER_TX_INST_CFG0_REG register, then write the word in the BITSCRAMBLER_TX_INST_CFG1_REG register. Note that the 257th bit is written as bit 0 into BITSCRAMBLER_TX_INST_CFG1_REG.
5. Load LUT into BitScrambler, if needed:
   (a) Configure BITSCRAMBLER_TX_LUT_MODE in BITSCRAMBLER_TX_LUT_CFG0_REG to set the LUT width
   (b) Write the address to the BITSCRAMBLER_TX_LUT_CFG0_REG
   (c) Write the data word or the byte itself to BITSCRAMBLER_TX_LUT_CFG1_REG

Note that it is acceptable to change the LUT width after writing the data and before starting the BitScrambler.

6. Configure BitScrambler. Dependent on what the BitScrambler program expects, you may need to set or clear the various bits in the BITSCRAMBLER_TX_CTRL_REG register. You may also need to set BITSCRAMBLER_TX_TAILING_BITS_REG to an applicable value.
7. Start the BitScrambler by clearing the BITSCRAMBLER_TX_HALT bit in the BITSCRAMBLER_TX_CTRL_REG register.
8. Start DMA transaction. Please refer to Chapter 5 GDMA Controller (GDMA) for more information about DMA subsystem and refer to the peripheral chapter if loopback mode is not used.
9. Wait until DMA transaction is done.
10. Halt the BitScrambler by setting the BITSCRAMBLER_TX_HALT in the BITSCRAMBLER_TX_CTRL_REG register.
11. Wait for halt state. The BitScrambler is halted when the BITSCRAMBLER_TX_IN_IDLE bit in the BITSCRAMBLER_TX_STATE_REG register is set.
```