

```markdown
Register 43.5. PARL_IO_TX_DATA_CFG_REG (0x0010)

| 31 | 29 | 28 | 27 | ... | 9 | 8 | ... | 0 |
|----:|----:|----:|----:|-----|---|---|-----|---|
| 0x3 | 0   |     |     | PARL_IO_TX_BITLEN | 0 | O | O | O | O | O | O | O | O | Reset |

PARL_IO_TX_BITLEN Configures the expected bit number of TXD. (R/W)

PARL_IO_TX_DATA_ORDER_INV Configures whether to invert the bit order of one byte sent from TX FIFO to IO data.
0: No effect
1: Invert
(R/W)

PARL_IO_TX_BUS_WID_SEL Configures the TXD bus width.
0: 1 bit
1: 2 bits
2: 4 bits
3: 8 bits
4 ~ 15: Invalid and will incur error
(R/W)

Register 43.6. PARL_IO_TX_START_CFG_REG (0x0014)

| 31 | 30 |
|----:|----:|
|    | PARL_IO_TX_START |

PARL_IO_TX_START Configures whether to start TX data transmission.
0: No effect
1: Start
(R/W)
```