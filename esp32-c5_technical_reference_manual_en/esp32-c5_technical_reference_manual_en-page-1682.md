

```markdown
Register 44.5. BITSCRAMBLER_TX_LUT_CFG0_REG (0x0010)

BITS scrambler TX LUT IDX Configures where in LUT RAM to access. Measurement unit: word size configured by BITSCRAMBLER_TX_LUT_MODE. (R/W)

BITS scrambler TX LUT MODE Configures the word size of LUT RAM for Bitscrambler programs.
O: 1 byte
1: 2 bytes
2: 4 bytes
3: Reserved
(R/W)
```

```markdown
Register 44.6. BITSCRAMBLER_TX_LUT_CFG1_REG (0x0014)

BITS scrambler TX LUT Configures the LUT entry to be accessed at the position specified by BITSCRAMBLER_TX_LUT_CFG0_REG. (R/W)
```