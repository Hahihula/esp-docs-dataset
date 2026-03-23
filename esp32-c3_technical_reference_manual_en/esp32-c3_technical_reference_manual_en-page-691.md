

```markdown
8. I2Cslave compares the slave address sent by I2Cmaster with its own address in I2C_SLAVE_ADDR (slave). When ack_check_en (master) in I2Cmaster's WRITE command is 1, I2Cmaster checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2Cmaster does not check ACK value and take I2Cslave as matching slave by default.

* Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2Cmaster continues data transfer.
* Not match: If the received ACK value does not match ack_exp, I2Cmaster generates an I2C_NACK_INT (master) interrupt and stops data transfer.

9. I2Cmaster sends data, and checks ACK value or not according to ack_check_en (master).

10. If data to be sent is larger than 32 bytes, TX RAM of I2Cmaster may wrap around in FIFO mode. For details, please refer to Section 28.4.10.

11. If data to be received is larger than 32 bytes, RX RAM of I2Cslave may wrap around in FIFO mode. For details, please refer to Section 28.4.10.

If data to be received is larger than 32 bytes, the other way is to enable clock stretching by setting I2C_SLAVE_SCL_STRETCH_EN (slave) and clearing I2C_RX_FULL_ACK_LEVEL to 0. When RX RAM is full, an I2C_SLAVE_STRETCH_INT (slave) interrupt is generated. In this way, I2Cslave can hold SCL low, in exchange for more time to read data. After software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.

12. After data transfer completes, I2Cmaster executes the STOP command, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.
```