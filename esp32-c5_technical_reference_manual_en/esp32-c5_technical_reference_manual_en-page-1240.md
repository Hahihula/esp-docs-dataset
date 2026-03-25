

```markdown
Register 34.14. I2C_FIFO_CONF_REG (0x0018)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 15  | I2C_FIFO_PRT_EN                                                              |
| 14  | I2C_TX_FIFO_RST                                                             |
| 13  | I2C_RX_FIFO_RST                                                             |
| 12  | I2C_FIFO_ADDR_CFG_EN                                                       |
| 11  | I2C_NONFIFO_EN                                                              |
| 10  | I2C_TXFIFO_WM_THRHD                                                         |
| 9   | I2C_RXFIFO_WM_THRHD                                                         |
| 8-4 | (reserved)                                                                  |
| 3   | 0x4                                                                         |
| 2   | 0xB                                                                         |
| 1   | Reset                                                                       |
| 0   | No effect                                                                   |

I2C_RXFIFO_WM_THRHD Configures the watermark threshold of RX FIFO in non-FIFO access mode.
When I2C_FIFO_PRT_EN is 1 and RX FIFO counter is bigger than I2C_RXFIFO_WM_THRHD[4:0],
I2C_RXFIFO_WM_INT_RAW bit will be valid. (R/W)

I2C_TXFIFO_WM_THRHD Configures the watermark threshold of TX FIFO in non-FIFO access mode.
When I2C_FIFO_PRT_EN is 1 and TC FIFO counter is bigger than I2C_TXFIFO_WM_THRHD[4:0],
I2C_TXFIFO_WM_INT_RAW bit will be valid. (R/W)

I2C_NONFIFO_EN Configures to enable APB non-FIFO access. (R/W)

I2C_FIFO_ADDR_CFG_EN Configures the slave to enable dual address mode. When this mode is enabled,
the byte received after the I2C address byte represents the offset address in the I2C Slave RAM.
0: Disable
1: Enable
(R/W)

I2C_RX_FIFO_RST Configures to reset RX FIFO.
0: No effect
1: Reset
(R/W)

I2C_TX_FIFO_RST Configures to reset TX FIFO.
0: No effect
1: Reset
(R/W)

I2C_FIFO_PRT_EN Configures to enable FIFO pointer in non-FIFO access mode. This bit controls the valid bits and the TX/RX FIFO overflow, underflow, full and empty interrupts.
0: No effect
1: Enable
(R/W)
```