

```markdown
4. Write I2C<sub>slave</sub> address and data to be sent to TX RAM of I2C<sub>master</sub> in either FIFO mode or non-FIFO mode according to Section 28.4.10.
5. Write address of I2C<sub>slave</sub> to I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) register.
6. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
7. Write 1 to I2C_TRANS_START (master) and I2C_TRANS_START (slave) to start transfer.
8. I2C<sub>slave</sub> compares the slave address sent by I2C<sub>master</sub> with its own address in I2C_SLAVE_ADDR (slave). When ack_check_en (master) in I2C<sub>master</sub>'s WRITE command is 1, I2C<sub>master</sub> checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2C<sub>master</sub> does not check ACK value and take I2C<sub>slave</sub> as a matching slave by default.
    * Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2C<sub>master</sub> continues data transfer.
    * Not match: If the received ACK value does not match ack_exp, I2C<sub>master</sub> generates an I2C_NACK_INT (master) interrupt and stops data transfer.
9. I2C<sub>master</sub> sends data, and checks ACK value or not according to ack_check_en (master).
10. If data to be sent (N) is larger than 32 bytes, TX RAM of I2C<sub>master</sub> may wrap around in FIFO mode. For details, please refer to Section 28.4.10.
11. If data to be received (N) is larger than 32 bytes, RX RAM of I2C<sub>slave</sub> may wrap around in FIFO mode. For details, please refer to Section 28.4.10.
    If data to be received (N) is larger than 32 bytes, the other way is to enable clock stretching by setting the I2C_SLAVE_SCL_STRETCH_EN (slave), and clearing I2C_RX_FULL_ACK_LEVEL. When RX RAM is full, an I2C_SLAVE_STRETCH_INT (slave) interrupt is generated. In this way, I2C<sub>slave</sub> can hold SCL low, in exchange for more time to read data. After software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.
12. After data transfer completes, I2C<sub>master</sub> executes the STOP command, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.

## 28.5.2 I2C<sub>master</sub> Writes to I2C<sub>slave</sub> with a 10-bit Address in One Command Sequence
```