Title: Chapter 27 I2C Controller (I2C)

Body Text:
Figure 27.5-3 shows how I2C_master writes N bytes of data to I2C_slave registers on RAM using 7-bit double addressing. The configuration and transfer process is similar to what is described in Section **27.5.1**, except that in 7-bit double addressing mode, the master sends two 7-bit addresses. The first address is the address of an I2C slave, and the second one is I2C_slave's memory address (i.e., addrM in Figure 27.5-3). When using double addressing, RAM must be accessed in non-FIFO mode. The I2C slave put received byte0 ~ byte(N-1) into its RAM in an order staring from addrM. The RAM is overwritten every 32 bytes.

Subtitle: **27.5.3.2 Configuration Example**

List:
1. Set `I2C_MS_MODE` (master) to 1, and `I2C_MS_MODE` (slave) to 0.
2. Set `I2C_FIFO_ADDR_CFG_EN` (slave) to 1 to enable double addressing mode.

Body Text:

3. Write 1 to `I2C_CONF_UPGRADE` (master) and `I2C_CONF_UPGRADE` (slave) to synchronize registers.

4. Configure command registers of I2C_master.
- Command registers
| command code | ack_value | ack_exp | ack_check_err | byte_num |
|---------------|-----------|---------|----------------|----------|
| I2C_COMMANDO  | RSTART   | —       |                |          |
| I2C_COMMAND1  | WRITE    | ack_value | ack_exp        | N+2      |
| I2C_COMMAND2  | STOP     | —       |                |          |

5. Write the address of `I2C_slave` and data to be sent to TX RAM of `I2C_master` FIFO or non-FIFO mode.

6. Write the address of `I2C_slave` to `I2C_SLAVE_ADDR` (slave) in `I2C_SLAVE_ADDR_REG` (slave) register.
- Write 1 to `I2C_CONF_UPGRADE` (master) and `I2C_CONF_UPGRADE` (slave) to synchronize registers.

7. Write 1 to `I2C_TRANS_START` (master) and `I2CTrans_START` (slave) to start transfer.

8. I2C_slave compares the slave address sent by `I2C_master` with its own address in `I2C_SLAVE_ADDR` (slave). When ack_check_en (master) in `I2C_master`'s WRITE command is 1, `I2C_master` checks ACK value each time it sends a byte. When ack_check_en (master) is 0, `I2C_master` does not check ACK value and take `I2C_slave` as matching slave by default.
- Match: If the received ACK value matches ack_exp (master) (the expected ACK value), `I2C_master` continues data transfer.

- Not match: If the received ACK value does not match ack_exp, `I2C_master` generates an I2C_NACK_INT (master) interrupt and stops data transfer.
- 10. `I2C_slave` receives the RX RAM address sent by `I2C_master` and adds the offset.

11. `I2C_master` sends data, and checks ACK value or not according to ack_check_en (master).

12. If data to be sent is larger than 32 bytes, TX RAM of `I2C_master` may wrap around in FIFO mode. For details, please refer to Section **27.4.10**.

13. If data to be received is larger than 32 bytes, you may enable clock stretching by setting `I2C_SLAVE_SCL_STRETCH_EN` (slave), and clearing `I2C_RX_FULL_ACK_LEVEL` to O. When RX RAM is full, an `I2C_SLAVE_STRETCH_INT` (slave) interrupt is generated. In this way, `I2C_slave` can hold SCL low, in exchange for more time to read data. After software has finished reading I, you can set

Footer:
Espressif Systems
1001 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback