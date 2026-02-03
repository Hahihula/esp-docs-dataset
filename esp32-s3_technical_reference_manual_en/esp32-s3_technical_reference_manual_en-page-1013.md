Title: Chapter 27 I2C Controller (I2C)

Body Text:
Transfer finishes and an I2C_END_DETECT_INT interrupt is detected, the cmd box is configured as shown in Segment2. Once I2CTransStart is set, l2c_master terminates the transfer by sending a STOP bit.

Subtitle: 27.5.8.2 Configuration Example

1. Set `I2C_MS_MODE` (master) to 1 and `I2C_MS_MODE` (slave) to 0.
2. We recommend setting `I2C_SLAVE_SCL_STRETCH_EN` (slave) to 1, so that SCL can be held low for more processing time when I2cSlave needs to send data. If this bit is not set, software should write data to be sent to l2c_slave’s TX RAM before l2c_master initiates transfer. Configuration below is applicable to scenario where `I2C_SLAVE_SCL_STRETCH_EN` (slave) is 1.
3. Write 1 to `I2C_CONF_UPGRADE` (master) and `I2C_CONF_UPGRADE` (slave) to synchronize registers.

4. Configure command registers of I2c_master:

| Command registers | code | ack_value | ack_exp | ack_check_err | byte_num |
|--------------------|------|----------|--------|---------------|---------|
| l2c_master         |      |          |        |               |         |
| `I2C_COMMAND0`     (master) | RSTART | —       | 0      | —             | N       |
| `I2C_COMMAND1`     (master) | WRITE | O       | 0      | 1             | 1       |
| `I2C_COMMAND2`     (master) | READ  | O       | 0      | 1             | N       |
| `I2C_COMMAND3`     (master) | END   | —       | —      |               |         |

5. Write the address of I2cSlave to TX RAM of l2c_master in FIFO or non-FIFO mode.
6. Write the address of I2cSlave to `I2C_SLAVE_ADDR` (slave) in `I2C_SLAVE_ADDR_REG` (slave) register.
7. Write 1 to `I2C_CONF_UPGRADE` (master) and `I2C_CONF_UPGRADE` (slave) to synchronize registers.

8. Write 1 to `I2CTransStart` (master) to start l2c_master’s transfer.

9. Start I2cSlave’s transfer according to Section 27.4.14.
10. I2cSlave compares the slave address sent by l2c_master with its own address in `I2C_SLAVE_ADDR` (slave). When ack_check_en (master) in l2c_master’s WRITE command is 1, l2c_master checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2cMaster does not check ACK value and take I2cSlave as matching slave by default.
    - Match: If the received ACK value matches ack_exp (master) (the expected ACK value), l2c_master continues data transfer.

11. Not match: If the received ACK value does not match ack_exp, l2c_master generates an `I2C_NACK_INT` (master) interrupt and stops data transfer.
    - After I2C_SLAVE_STRETCH_INT (slave) is generated, the `I2C.StretchCause` bit is 0. The address of I2cSlave matches the address sent over SDA, and l2cSlave needs to send data.

12. Write data to be sent to TX RAM of I2cSlave in either FIFO mode or non-FIFO mode according to Section 27.4.10.
13. Set `I2C_SLAVE_SCL_STRETCH_CLR` (slave) to 1 to release SCL.

Footer:
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback