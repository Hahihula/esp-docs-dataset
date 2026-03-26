

```markdown
Register 59.7. BITSCRAMBLER_RX_LUT_CFG0_REG (0x0018)

BITS0: Reserved
BIT12-10: BITSCRAMBLER_RX_LUT_MODE
BIT0: BITSCRAMBLER_RX_LUT_IDX

BITS0: Reset

BITS0: 0

BITS0: Reserved

BITS0: Configures where in LUT RAM to access. Measurement unit: word size configured by BITSCRAMBLER_RX_LUT_MODE. (R/W)

BITS0: Configures the word size of LUT RAM for BitScrambler programs.
O: 1 byte
1: 2 bytes
2: 4 bytes
3: Reserved
(R/W)
```

```markdown
Register 59.8. BITSCRAMBLER_RX_LUT_CFG1_REG (0x001C)

BITS0-28: Reserved

BITS0: Reset

BITS0: Configures the LUT entry to be accessed at the position specified by BITSCRAMBLER_RX_LUT_CFG0_REG. (R/W)
```