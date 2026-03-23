

```markdown
Register 28.19. I2C_SR_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | I2C_SCL_STATE_LAST | (reserved) | I2C_SCL_MAIN_STATE_LAST | I2C_TXFIFO_CNT | (reserved) | I2C_STRETCH_CAUSE | (reserved) | I2C_RXFIFO_CNT | I2C_SLAVE_ADDRESSED | I2C_BUS_BUSY | I2C_ARB_LOST | (reserved) | I2C_SLAVE_RW | Reset |
| Value | 0 | 0 | 0 | 0 | 0 | 0x3 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

I2C_RESP_REC The received ACK value in master mode or slave mode. 0: ACK; 1: NACK. (RO)
I2C_SLAVE_RW When in slave mode, 0: master writes to slave; 1: master reads from slave. (RO)
I2C_ARB_LOST When the I2C controller loses control of the SCL line, this bit changes to 1. (RO)
I2C_BUS_BUSY 0: The I2C bus is in idle state; 1: The I2C bus is busy transferring data. (RO)
I2C_SLAVE_ADDRESSED When the I2C controller is in slave mode, and the address sent by the master matches the address of the slave, this bit is at high level. (RO)
I2C_RXFIFO_CNT This field represents the number of data bytes to be sent. (RO)
I2C_STRETCH_CAUSE The cause of SCL clock stretching in slave mode. 0: stretching SCL low when the master starts to read data; 1: stretching SCL low when TX FIFO is empty in slave mode; 2: stretching SCL low when RX FIFO is full in slave mode. (RO)
I2C_TXFIFO_CNT This field stores the number of data bytes received in RAM. (RO)
I2C_SCL_MAIN_STATE_LAST This field indicates the status of the state machine. 0: idle; 1: address shift; 2: ACK address; 3: receive data; 4: transmit data; 5: send ACK; 6: wait for ACK. (RO)
I2C_SCL_STATE_LAST This field indicates the status of the state machine used to produce SCL. 0: idle; 1: start; 2: falling edge; 3: low; 4: rising edge; 5: high; 6: stop. (RO)
```