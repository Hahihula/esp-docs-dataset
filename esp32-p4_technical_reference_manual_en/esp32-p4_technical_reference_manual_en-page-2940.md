

```markdown
Register 58.17. PARL_IO_TX_STO_REG (0x0040)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        |                                                                             |
|           |                                                                             |
| 13-12     | OxC00                                                                        |
|           | Reset                                                                       |
|           | Ox0                                                                          |
|           | 0 0 0 0 0 0 0                                                              |

PARL_IO_TX_CNT Represents the cycle number of reading the TX FIFO. (RO)
PARL_IO_TX_FIFO_RD_BIT_CNT Represents the bit number currently read from the TX FIFO. (RO)

Register 58.18. PARL_IO_RX_CLK_CFG_REG (0x0044)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        |                                                                             |
|           |                                                                             |
| 30-29     | O 0 0 0 ... 0                                                               |
|           | Reset                                                                       |
|           | 0 0 0 0 0 0 0                                                              |

PARL_IO_RX_CLK_INV Configures whether to invert the RX input Core clock.
O: No effect
1: Invert
(R/W)

PARL_IO_RX_CLK_O_INV Configures whether to invert the RX output Core clock.
O: No effect
1: Invert
(R/W)
```