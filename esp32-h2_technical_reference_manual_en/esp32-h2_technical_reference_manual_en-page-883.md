

```markdown
Register 30.18. I2C_SR_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | I2C_SCL_STATE_LAST | (reserved) | I2C_SCL_MAIN_STATE_LAST | I2C_TXFIFO_CNT | (reserved) | I2C_STRETCH_CAUSE | (reserved) | I2C_RXFIFO_CNT | (reserved) | I2C_SLAVE_ADDRESSED | I2C_BUS_BUSY | I2C_ARB_LOST | (reserved) | I2C_SLAVE_RW | I2C_RESP_REC | Reset |
| Value | 0 | 0 | 0 | 0 | 0 | 0x3 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

I2C_RESP_REC Represents the received ACK value in Master mode or Slave mode.
O: ACK
1: NACK (RO)

I2C_SLAVE_RW Represents the transfer direction in Slave mode.
O: Master writes to slave
1: Master reads from slave (RO)

I2C_ARB_LOST Represents whether the I2C controller loses control of SCL line.
O: No arbitration lost
1: Arbitration lost (RO)

I2C_BUS_BUSY Represents the I2C bus state.
O: The I2C bus is in idle state
1: The I2C bus is busy transferring data (RO)

I2C_SLAVE_ADDRESSED Represents whether the address sent by the master is equal to the address of the slave.
Valid only when the module is configured as an I2C Slave.
O: Not equal
1: Equal (RO)

I2C_RXFIFO_CNT Represents the number of data bytes received in RAM. (RO)

I2C_STRETCH_CAUSE Represents the cause of SCL clocking stretching in Slave mode.
O: Stretching SCL low when the master starts to read data.
1: Stretching SCL low when I2C TX FIFO is empty in Slave mode.
2: Stretching SCL low when I2C RX FIFO is full in Slave mode. (RO)

I2C_TXFIFO_CNT Represents the number of data bytes to be sent. (RO)

Continued on the next page...
```