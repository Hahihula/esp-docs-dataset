

```markdown
| Command registers | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|:-------------------|:---------|:-----------|:---------|:-------------|:----------|
| I2C_COMMANDO (master) | RSTART  | —         | —       | —           | —        |
| I2C_COMMAND1 (master) | WRITE   | ack_value | ack_exp | 1           | N+2      |
| I2C_COMMAND2 (master) | STOP    | —         | —       | —           | —        |

4. Configure `I2C_SLAVE_ADDR` (slave) in `I2C_SLAVE_ADDR_REG` (slave) as `I2C_slave`’s 10-bit address, and set `I2C_ADDR_10BIT_EN` (slave) to 1 to enable 10-bit addressing.
5. Write the address of `I2C_slave` and data to be sent to TX RAM of `I2C_master`. The first byte of the address of `I2C_slave` comprises ((0x78 | I2C_SLAVE_ADDR[9:8])«1) and a R/W bit. The second byte of the address of `I2C_slave` is `I2C_SLAVE_ADDR[7:0]`. These two bytes are followed by data to be sent in FIFO or non-FIFO mode.
6. Write 1 to `I2C_CONF_UPGATE` (master) and `I2C_CONF_UPGATE` (slave) to synchronize registers.
7. Write 1 to `I2C_TRANS_START` (master) and `I2C_TRANS_START` (slave) to start transfer.
8. `I2C_slave` compares the slave address sent by `I2C_master` with its own address in `I2C_SLAVE_ADDR` (slave). When `ack_check_en` (master) in `I2C_master`’s WRITE command is 1, `I2C_master` checks ACK value each time it sends a byte. When `ack_check_en` (master) is 0, `I2C_master` does not check the ACK value and take `I2C_slave` as a matching slave by default.
    * Match: If the received ACK value matches `ack_exp` (master) (the expected ACK value), `I2C_master` continues data transfer.
    * Not match: If the received ACK value does not match `ack_exp`, `I2C_master` generates an `I2C_NACK_INT` (master) interrupt and stops data transfer.
9. `I2C_master` sends data, and determines whether to check ACK value according to `ack_check_en` (master).
10. If data to be sent is larger than TX FIFO depth, TX RAM of `I2C_master` may wrap around in FIFO mode. For details, please refer to Section 34.4.10.
11. If data to be received is larger than RX FIFO depth, RX RAM of `I2C_slave` may wrap around in FIFO mode. For details, please refer to Section 34.4.10.

    If data to be received is larger than RX FIFO depth, the other way is to enable clock stretching by setting `I2C_SLAVE_SCL_STRETCH_EN` (slave), and clearing `I2C_RX_FULL_ACK_LEVEL` to 0. When RX RAM is full, an `I2C_SLAVE_STRETCH_INT` (slave) interrupt is generated. In this way, `I2C_slave` can hold SCL low, in exchange for more time to read data. After the software has finished reading, you can set `I2C_SLAVE_STRETCH_INT_CLR` (slave) to 1 to clear interrupt, and set `I2C_SLAVE_SCL_STRETCH_CLR` (slave) to release the SCL line.
12. After data transfer completes, `I2C_master` executes the STOP command, and generates an `I2C_TRANS_COMPLETE_INT` (master) interrupt.

## 34.7.3 I2C_master Writes to I2C_slave with Two 7-bit Addresses in One Command Sequence
```