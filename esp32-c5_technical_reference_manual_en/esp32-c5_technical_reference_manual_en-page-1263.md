

```markdown
Register 34.48. LP_I2C_FIFO_CONF_REG (0x0018)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | LP_I2C_RXFIFO_WM_THRDHD                                                     |
| 29  | LP_I2C_TXFIFO_WM_THRDHD                                                     |
| 28  | LP_I2C_NONFIFO_EN                                                           |
| 27  | LP_I2C_RX_FIFO_RST                                                          |
| 26  | LP_I2C_TX_FIFO_RST                                                          |
| 25  | LP_I2C_FIFO_PTR_EN                                                          |
| 15-4| (reserved)                                                                  |
| 3   | Reset                                                                      |

LP_I2C_RXFIFO_WM_THRDHD Configures the watermark threshold of RX FIFO in nonfifo access mode. When LP_I2C_FIFO_PTR_EN is 1 and RX FIFO counter is bigger than LP_I2C_RXFIFO_WM_THRH[3:0], LP_I2C_RXFIFO_WM_INT_RAW bit will be valid. (R/W)

LP_I2C_TXFIFO_WM_THRDHD Configures the watermark threshold of TX FIFO in nonfifo access mode. When LP_I2C_FIFO_PTR_EN is 1 and RX FIFO counter is bigger than LP_I2C_TXFIFO_WM_THRH[3:0], LP_I2C_TXFIFO_WM_INT_RAW bit will be valid. (R/W)

LP_I2C_NONFIFO_EN Configures to enable APB nonfifo access. (R/W)

LP_I2C_RX_FIFO_RST Configures to reset RX FIFO.
  0: No effect
  1: Reset
  (R/W)

LP_I2C_TX_FIFO_RST Configures to reset TX FIFO.
  0: No effect
  1: Reset
  (R/W)

LP_I2C_FIFO_PTR_EN Configures to enable FIFO pointer in nonfifo access mode. This bit controls the valid bits and the TX/RX FIFO overflow, underflow, full and empty interrupts.
  0: No effect
  1: Enable
  (R/W)
```