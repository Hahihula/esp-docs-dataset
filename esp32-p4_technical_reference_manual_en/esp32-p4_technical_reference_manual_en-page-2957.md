

# 59.7 Registers

The addresses in this section are relative to the Bit-scrambler base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 59.1. BITSCRAMBLER_TX_INST_CFGO_REG (0x0000)

```
31                                 7 6     3 2      0
+-----------------------------------------------+
| (reserved) | BITSCRAMBLER_TX_INST_POS | BITSCRAMBLER_TX_INST_IDX |
+-----------------------------------------------+
```

**BITSCRAMBLER_TX_INST_IDX** Configures the index of the BitScrambler instruction to be accessed via `BITSCRAMBLER_TX_INST_CFG1_REG`. (R/W)

**BITSCRAMBLER_TX_INST_POS** Configures the offset into the 257-bit BitScrambler instruction (in 32-bit increments) to be accessed via `BITSCRAMBLER_TX_INST_CFG1_REG`. (R/W)

## Register 59.2. BITSCRAMBLER_TX_INST_CFG1_REG (0x0004)

```
31                                 4
+-----------------------------------------------+
| BITSCRAMBLER_TX_INST | Reset |
+-----------------------------------------------+
```

**BITSCRAMBLER_TX_INST** Configures the instruction to be accessed at the address specified by `BITSCRAMBLER_TX_INST_CFGO_REG`. (R/W)