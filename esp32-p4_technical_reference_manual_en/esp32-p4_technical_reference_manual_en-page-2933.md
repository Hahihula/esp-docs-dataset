

```markdown
Register 58.2. PARL_IO_RX_DATA_CFG_REG (0x0004)

| 31 | 29 | 28 | 27 | ... | 9 | 8 | ... | 0 |
|----:|----:|----:|----:|-----|---|---|-----|---|
| Ox3 |    0 |     |     |      |   |   |      | Reset |

PARL_IO_RX_BITLEN Configures the expected bit number of RXD. (R/W)

PARL_IO_RX_DATA_ORDER_INV Configures whether to invert the bit order of one byte sent from RX FIFO to GDMA. (R/W)

PARL_IO_RX_BUS_WID_SEL Configures the RXD bus width.
0: 1 bit
1: 2 bits
2: 4 bits
3: 8 bits
4: 16 bits
5 ~ 15: Invalid and will incur error
(R/W)
```