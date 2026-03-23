
```markdown
Register 28.14. I2C_FIFO_CONF_REG (0x0018)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 15  | I2C_FIFO_PRT_EN                                                             |
| 14  | I2C_TX_FIFO_RST                                                              |
| 13  | I2C_RX_FIFO_RST                                                              |
| 12  | I2C_RX_FIFO_ADDR_CFG_EN                                                     |
| 11  | I2C_NONFIFO_EN                                                               |
| 10  | I2C_TXFIFO_WM_THRHD                                                          |
| 5   | I2C_RXFIFO_WM_THRHD                                                          |
| 4   | Reset                                                                       |
|     | 0x4                                                                         |
|     | 0xb                                                                         |

I2C_RXFIFO_WM_THRHD The watermark threshold of RX FIFO in non-FIFO mode. When I2C_FIFO_PRT_EN is 1 and RX FIFO counter is bigger than I2C_RXFIFO_WM_THRHD[4:0], I2C_RXFIFO_WM_INT_RAW bit is valid. (R/W)

I2C_TXFIFO_WM_THRHD The watermark threshold of TX FIFO in non-FIFO mode. When I2C_FIFO_PRT_EN is 1 and TX FIFO counter is smaller than I2C_TXFIFO_WM_THRHD[4:0], I2C_TXFIFO_WM_INT_RAW bit is valid. (R/W)

I2C_NONFIFO_EN Set this bit to enable APB non-FIFO mode. (R/W)

I2C_FIFO_ADDR_CFG_EN When this bit is set to 1, the byte received after the I2C address byte represents the offset address in the I2C Slave RAM. (R/W)

I2C_RX_FIFO_RST Set this bit to reset RX FIFO. (R/W)

I2C_TX_FIFO_RST Set this bit to reset TX FIFO. (R/W)

I2C_FIFO_PRT_EN The control enable bit of FIFO pointer in non-FIFO mode. This bit controls the valid bits and TX/RX FIFO overflow, underflow, full and empty interrupts. (R/W)


Register 28.15. I2C_FILTER_CFG_REG (0x0050)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 10  | I2C_SDA_FILTER_THRES                                                       |
| 9   | I2C_SCL_FILTER_THRES                                                       |
| 8   | I2C_SCL_FILTER_EN                                                           |
| 7   | I2C_SDA_FILTER_EN                                                           |
| 6   | (reserved)                                                                  |
| 5   | (reserved)                                                                  |
| 4   | (reserved)                                                                  |
| 3   | (reserved)                                                                  |
| 2   | (reserved)                                                                  |
| 1   | (reserved)                                                                  |
| 0   | Reset                                                                       |
|     | 0                                                                             |

I2C_SCL_FILTER_THRES When a pulse on the SCL input has smaller width than the value of this field in I2C module clock cycles, the I2C controller ignores that pulse. (R/W)

I2C_SDA_FILTER_THRES When a pulse on the SDA input has smaller width than the value of this field in I2C module clock cycles, the I2C controller ignores that pulse. (R/W)

I2C_SCL_FILTER_EN This is the filter enable bit for SCL. (R/W)

I2C_SDA_FILTER_EN This is the filter enable bit for SDA. (R/W)
```