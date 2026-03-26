

```markdown
| Register                                 | EOF-on-N-reads | EOF-on-N-writes |
|------------------------------------------|:---------------|:----------------|
| BITSRCRAMBLER_TX_RD_DUMMY               | 1              | 1               |
| BITSRCRAMBLER_TX_FETCH_MODE             | 0              | 0               |
| BITSRCRAMBLER_TX_EOF_MODE               | 1              | 0               |
| BITSRCRAMBLER_TX_HALT_MODE              | 1              | 1               |

## 59.5 Programming Procedures

Note that these instructions are written for a TX BitScrambler, which is in the memory-to-peripheral path, or memory-to-memory path if in loopback mode. For the peripheral-to-memory path, the RX BitScrambler is used. Unless otherwise indicated, you can exchange "TX" for "RX" in these instructions to configure the RX BitScrambler.

1.  Attach the BitScrambler to a peripheral by configuring HP_SYSTEM_BITSCRAMBLER_PERI_TX_SEL field in HP_SYSTEM_BITSCRAMBLER_PERI_SEL_REG register. Note that this step is required even in loopback mode.
2.  Enable the BitScrambler by setting the BITSRCRAMBLER_TX_ENA field in the BITSRCRAMBLER_TX_CTRL_REG register.
3.  Configure loopback mode if required. If loopback mode is needed, set BITSRCRAMBLER_LOOP_MODE in the BITSRCRAMBLER_SYS_REG register. Otherwise, clear it.
4.  Load program into BitScrambler. For each instruction and each 32-bit word within the instruction, set the BITSRCRAMBLER_TX_INST_IDX and BITSRCRAMBLER_TX_INST_POS fields in the BITSRCRAMBLER_TX_INST_CFG0_REG register, then write the word in the BITSRCRAMBLER_TX_INST_CFG1_REG register. Note that the 257th bit is written as bit 0 into BITSRCRAMBLER_TX_INST_CFG1_REG.
5.  Load LUT into BitScrambler, if needed:
    (a) Configure BITSRCRAMBLER_TX_LUT_MODE in BITSRCRAMBLER_TX_LUT_CFG0_REG to set the LUT width
    (b) Write the address to the BITSRCRAMBLER_TX_LUT_CFG0_REG
    (c) Write the data word or the byte itself to BITSRCRAMBLER_TX_LUT_CFG1_REG

Note that it is acceptable to change the LUT width after writing the data and before starting the BitScrambler.
6.  Configure BitScrambler. Dependent on what the BitScrambler program expects, you may need to set or clear the various bits in the BITSRCRAMBLER_TX_CTRL_REG register. You may also need to set BITSRCRAMBLER_TX_TAILING_BITS_REG to an applicable value.
```