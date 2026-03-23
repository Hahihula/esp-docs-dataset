

```markdown
transfer finishes and an I2C_END_DETECT_INT interrupt is detected, the cmd box is configured as shown in Segment2. Once I2C_TRANS_START is set, I2Cmaster terminates the transfer by sending a STOP bit.

### 29.6.8.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. We recommend setting I2C_SLAVE_SCL_STRETCH_EN (slave) to 1, so that SCL can be held low for more processing time when I2Cslave needs to send data. If this bit is not set, software should write data to be sent to I2Cslave’s TX RAM before I2Cmaster initiates transfer. Configuration below is applicable to scenario where I2C_SLAVE_SCL_STRETCH_EN (slave) is 1.
3. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
4. Configure command registers of I2Cmaster.

| Command registers of I2Cmaster | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|-------------------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMAND0 (master)         | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master)         | WRITE   | 0         | 0       | 1            | 1        |
| I2C_COMMAND2 (master)         | READ    | 0         | 0       | 1            | N        |
| I2C_COMMAND3 (master)         | END     | —         | —       | —            | —        |

5. Write the address of I2Cslave to TX RAM of I2Cmaster in FIFO or non-FIFO mode.
6. Write the address of I2Cslave to I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) register.
7. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
8. Write 1 to I2C_TRANS_START (master) to start I2Cmaster’s transfer.
9. Start I2Cslave’s transfer according to Section 29.4.14.
10. I2Cslave compares the slave address sent by I2Cmaster with its own address in I2C_SLAVE_ADDR (slave). When ack_check_en (master) in I2Cmaster’s WRITE command is 1, I2Cmaster checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2Cmaster does not check ACK value and take I2Cslave as matching slave by default.

    * Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2Cmaster continues data transfer.
    * Not match: If the received ACK value does not match ack_exp, I2Cmaster generates an I2C_NACK_INT (master) interrupt and stops data transfer.

11. After I2C_SLAVE_STRETCH_INT (slave) is generated, the I2C_STRETCH_CAUSE bit is 0. The address of I2Cslave matches the address sent over SDA, and I2Cslave needs to send data.
12. Write data to be sent to TX RAM of I2Cslave in either FIFO mode or non-FIFO mode according to Section 29.4.10.
13. Set I2C_SLAVE_SCL_STRETCH_CLR (slave) to 1 to release SCL.
```