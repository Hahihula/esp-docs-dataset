

```markdown
Register 28.20. I2C_FIFO_ST_REG (0x0014)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0   | 0   |    |    |    |    |    |    |    | I2C_SLAVE_RW_POINT | (reserved) | I2C_TXFIFO_WADDR |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
| Reset|

I2C_RXFIFO_RADDR  This is the offset address of the APB reading from RX FIFO. (RO)
I2C_RXFIFO_WADDR  This is the offset address of the I2C controller receiving data and writing to RX FIFO. (RO)
I2C_TXFIFO_RADDR  This is the offset address of the I2C controller reading from TX FIFO. (RO)
I2C_TXFIFO_WADDR  This is the offset address of APB bus writing to TX FIFO. (RO)
I2C_SLAVE_RW_POINT  The received data in I2C slave mode. (RO)

Register 28.21. I2C_DATA_REG (0x001C)

| 31 | 30 | 29 | ... | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----:|----:|----:|-----:|----:|----:|----:|----:|----:|----:|----:|----:|
| (reserved) | ... | I2C_FIFO_RDATA |

I2C_FIFO_RDATA  This field is used to read data from RX FIFO, or write data to TX FIFO. (R/W)
```