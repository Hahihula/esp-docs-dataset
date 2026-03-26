

```markdown
Register 59.3. BITSCRAMBLER_RX_INST_CFG0_REG (0x0008)

| 31 | 7 | 6 | 3 | 2 | 0 |
|----:|:-|:-|:-|:-|---|
|    |    |    |    | Reset |

BITS scrambler RX INST IDX Configures the index of the BitScrambler instruction to be accessed via BITSCRAMBLER_RX_INST_CFG1_REG. (R/W)

BITS scrambler RX INST POS Configures the offset into the 257-bit BitScrambler instruction (in 32-bit increments) to be accessed via BITSCRAMBLER_RX_INST_CFG1_REG. (R/W)


Register 59.4. BITSCRAMBLER_RX_INST_CFG1_REG (0x000C)

| 31 | 12 | 0 |
|----:|:-|---|
|    | Reset |

BITS scrambler RX INST Configures the instruction to be accessed at the address specified by BITSCRAMBLER_RX_INST_CFG0_REG. (R/W)
```