

```markdown
- Not match: If the received ACK value does not match ack_exp, I2C_master generates an I2C_NACK_INT (master) interrupt and stops data transfer.
11. After I2C_SLAVE_STRETCH_INT (slave) is generated, the I2C_STRETCH_CAUSE bit is 0. The I2C_slave address matches the address sent over SDA, and I2C_slave needs to send data.
12. Write data to be sent to TX RAM of I2C_slave according to Section 28.4.10.
13. Set I2C_SLAVE_SCL_STRETCH_CLR (slave) to 1 to release SCL.
14. I2C_slave sends data, and I2C_master checks ACK value or not according to ack_check_en (master) in the READ command.
15. If data to be read by I2C_master is larger than 32 bytes, an I2C_SLAVE_STRETCH_INT (slave) interrupt will be generated when TX RAM of I2C_slave becomes empty. In this way, I2C_slave can hold SCL low, so that software has more time to pad data in TX RAM of I2C_slave and read data in RX RAM of I2C_master. After software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.
16. After I2C_master has received the last byte of data, set ack_value (master) to 1. I2C_slave will stop transfer once receiving the I2C_NACK_INT interrupt.
17. After data transfer completes, I2C_master executes the STOP command, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.

## 28.5.6 I2C_master Reads I2C_slave with a 10-bit Address in One Command Sequence

### 28.5.6.1 Introduction

Figure 28.5-6. I2C_master Reading I2C_slave with a 10-bit Address
```