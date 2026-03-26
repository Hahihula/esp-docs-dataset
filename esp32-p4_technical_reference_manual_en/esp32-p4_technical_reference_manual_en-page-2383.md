

```markdown
Chapter 44 I2C Controller (I2C) GoBack

warnings. The address pointer wraps around to the beginning of the memory space once the end is reached.

44.6.7.2 Configuration Example

1. Set `I2C_MS_MODE` (master) to 1, and `I2C_MS_MODE` (slave) to 0.
2. We recommend setting `I2C_SLAVE_SCL_STRETCH_EN` (slave) to 1, so that SCL can be held low for more processing time when I2C_slave needs to send data. If this bit is not set, the software should write data to be sent to I2C_slave’s TX RAM before I2C_master initiates the transfer. The configuration below is applicable to the scenario where `I2C_SLAVE_SCL_STRETCH_EN` (slave) is 1.
3. Set `I2C_FIFO_ADDR_CFG_EN` (slave) to 1 to enable dual address mode.
4. Write 1 to `I2C_CONF_UPGATE` (master) and `I2C_CONF_UPGATE` (slave) to synchronize registers.
5. Configure command registers of I2C_master.

| Command registers of I2C_master | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|----------------------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMANDO (master)           | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master)           | WRITE   | 0         | 0       | 1            | 2        |
| I2C_COMMAND2 (master)           | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND3 (master)           | WRITE   | 0         | 0       | 1            | 1        |
| I2C_COMMAND4 (master)           | READ    | 0         | 0       | 1            | N-1      |
| I2C_COMMAND5 (master)           | READ    | 1         | 0       | 1            | 1        |
| I2C_COMMAND6 (master)           | STOP    | —         | —       | —            | —        |

6. Configure `I2C_SLAVE_ADDR` (slave) in `I2C_SLAVE_ADDR_REG` (slave) register as I2C_slave’s 7-bit address, and set `I2C_ADDR_10BIT_EN` (slave) to 0 to enable 7-bit addressing.
7. Write the address of I2C_slave and data to be sent to TX RAM of I2C_master in either FIFO or non-FIFO mode according to Section 44.4.10. The first byte of address comprises (`I2C_SLAVE_ADDR[6:0]`) «1) and a R/W bit, which is 0 and indicates a WRITE. The second byte of the address is memory address M of I2C_slave. The third byte is (`I2C_SLAVE_ADDR[6:0]`) «1) and a R/W bit, which is 1 and indicates a READ.
8. Write 1 to `I2C_CONF_UPGATE` (master) and `I2C_CONF_UPGATE` (slave) to synchronize registers.
9. Write 1 to `I2C_TRANS_START` (master) to start I2C_master’s transfer.
10. Start I2C_slave’s transfer according to Section 44.4.14.
11. I2C_slave compares the slave address sent by I2C_master with its own address in `I2C_SLAVE_ADDR` (slave). When ack_check_en (master) in I2C_master’s WRITE command is 1, I2C_master checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2C_master does not check ACK value and takes I2C_slave as a matching slave by default.

Espressif Systems          2383
Submit Documentation Feedback    ESP32-P4 TRM PRELIMINARY
```