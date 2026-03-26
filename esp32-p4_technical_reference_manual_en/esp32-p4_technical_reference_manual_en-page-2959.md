

```markdown
Register 59.5. BITSCRAMBLER_TX_LUT_CFG0_REG (0x0010)

BITS0: Reserved
BIT12-11: BITSCRAMBLER_TX_LUT_MODE
BIT10: BITSCRAMBLER_TX_LUT_IDX

| Bit | Description |
|-----|-------------|
| 31  | Reset       |

BITS0: Reserved
BIT12-11: BITSCRAMBLER_TX_LUT_MODE (R/W)
0: 1 Byte
1: 2 Bytes
2: 4 Bytes
3: Reserved

BIT10: BITSCRAMBLER_TX_LUT_IDX Configures where in LUT RAM to access. Measurement unit: word size configured by BITSCRAMBLER_TX_LUT_MODE.

Register 59.6. BITSCRAMBLER_TX_LUT_CFG1_REG (0x0014)

BITS0-20: BITSCRAMBLER_TX_LUT

BITSCRAMBLER_TX_LUT Configures the LUT entry to be accessed at the position specified by BITSCRAMBLER_TX_LUT_CFG0_REG. (R/W)
```