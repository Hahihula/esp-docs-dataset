

```markdown
| Command registers | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|:-------------------|:---------|:-----------|:---------|:--------------|:----------|
| I2C_COMMANDO (master) | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master) | WRITE   | ack_value | ack_exp | 1            | N+2       |
| I2C_COMMAND2 (master) | STOP    | —         | —       | —            | —        |

5. Write the address of `I2C_slave` and data to be sent to TX RAM of `I2C_master` in FIFO or non-FIFO mode.
6. Write the address of `I2C_slave` to `I2C_SLAVE_ADDR (slave)` in the `I2C_SLAVE_ADDR_REG (slave)` register.
7. Write 1 to `I2C_CONF_UPGATE (master)` and `I2C_CONF_UPGATE (slave)` to synchronize registers.
8. Write 1 to `I2C_TRANS_START (master)` and `I2C_TRANS_START (slave)` to start transfer.
9. `I2C_slave` compares the slave address sent by `I2C_master` with its own address in `I2C_SLAVE_ADDR (slave)`. When `ack_check_en (master)` in `I2C_master`'s WRITE command is 1, `I2C_master` checks ACK value each time it sends a byte. When `ack_check_en (master)` is 0, `I2C_master` does not check ACK value and takes `I2C_slave` as a matching slave by default.
    * Match: If the received ACK value matches `ack_exp (master)` (the expected ACK value), `I2C_master` continues data transfer.
    * Not match: If the received ACK value does not match `ack_exp`, `I2C_master` generates an `I2C_NACK_INT (master)` interrupt and stops data transfer.
10. `I2C_slave` receives the RX RAM address sent by `I2C_master` and adds the offset.
11. `I2C_master` sends data, and determines whether to check ACK value according to `ack_check_en (master)`.
12. If data to be sent is larger than TX FIFO depth, TX RAM of `I2C_master` may wrap around in FIFO mode. For details, please refer to Section 30.4.10.
13. If data to be received is larger than RX FIFO depth, you may enable clock stretching by setting `I2C_SLAVE_SCL_STRETCH_EN (slave)`, and clearing `I2C_RX_FULL_ACK_LEVEL` to 0. When RX RAM is full, an `I2C_SLAVE_STRETCH_INT (slave)` interrupt is generated. In this way, `I2C_slave` can hold SCL low, in exchange for more time to read data. After the software has finished reading, you can set
```