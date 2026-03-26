

```markdown
Register 59.9. BITSCRAMBLER_TX_TAILING_BITS_REG (0x0020)

| Bit Range | Description         |
|-----------|---------------------|
| 31        | reserved            |
| 16-15     | BITSCRAMBLER_TX_TAILING_BITS |
|           |                     |
| 0         | Reset               |

BITSCRAMBLER_TX_TAILING_BITS Configures the length of extra data after getting EOF for the TX BitScrambler core. Measurement unit: bit. (R/W)

Register 59.10. BITSCRAMBLER_RX_TAILING_BITS_REG (0x0024)

| Bit Range | Description         |
|-----------|---------------------|
| 31        | reserved            |
| 16-15     | BITSCRAMBLER_RX_TAILING_BITS |
|           |                     |
| 0         | Reset               |

BITSCRAMBLER_RX_TAILING_BITS Configures the length of extra data after getting EOF for the BitScrambler RX core. Measurement unit: bit. (R/W)
```