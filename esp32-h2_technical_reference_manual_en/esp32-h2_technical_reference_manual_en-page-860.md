

```markdown
| I2C_COMMANDO (master) | RSTART | — | — | — | — |
|------------------------|--------|----|----|----|----|
| I2C_COMMAND1 (master)  | WRITE  | 0  | 0  | 1  | 1  |
| I2C_COMMAND2 (master)  | READ   | 0  | 0  | 1  | N-1|
| I2C_COMMAND3 (master)  | READ   | 1  | 0  | 1  | 1  |
| I2C_COMMAND4 (master)  | STOP   | —  | —  | —  | —  |
```

5. Write the address of `I2C_slave` to TX RAM of `I2C_master` in either FIFO mode or non-FIFO mode according to Section 30.4.10.

6. Write the address of `I2C_slave` to `I2C_SLAVE_ADDR` (slave) in the `I2C_SLAVE_ADDR_REG` (slave) register.

7. Write 1 to `I2C_CONE_UPGATE` (master) and `I2C_CONE_UPGATE` (slave) to synchronize registers.

8. Write 1 to `I2C_TRANS_START` (master) bit to start `I2C_master`’s transfer.

9. Start `I2C_slave`’s transfer according to Section 30.4.14.

10. `I2C_slave` compares the slave address sent by `I2C_master` with its own address in `I2C_SLAVE_ADDR` (slave). When `ack_check_en` (master) in `I2C_master`’s WRITE command is 1, `I2C_master` checks ACK value each time it sends a byte. When `ack_check_en` (master) is 0, `I2C_master` does not check the ACK value and takes `I2C_slave` as a matching slave by default.

    * Match: If the received ACK value matches `ack_exp` (master) (the expected ACK value), `I2C_master` continues data transfer.
    * Not match: If the received ACK value does not match `ack_exp`, `I2C_master` generates an `I2C_NACK_INT` (master) interrupt and stops data transfer.

11. After `I2C_SLAVE_STRETCH_INT` (slave) is generated, the `I2C_STRETCH_CAUSE` bit is 0. The address of `I2C_slave` matches the address sent over SDA, and `I2C_slave` needs to send data.

12. Write data to be sent to TX RAM of `I2C_slave` in either FIFO mode or non-FIFO mode according to Section 30.4.10.

13. Set `I2C_SLAVE_SCL_STRETCH_CLR` (slave) to 1 to release SCL.

14. `I2C_slave` sends data, and `I2C_master` checks ACK value or not according to `ack_check_en` (master) in the READ command.

15. If data to be read by `I2C_master` is larger than the TX FIFO depth of `I2C_slave`, an `I2C_SLAVE_STRETCH_INT` (slave) interrupt will be generated when TX RAM of `I2C_slave` becomes empty. In this way, `I2C_slave` can hold SCL low, so that software has more time to pad data in TX RAM of `I2C_slave` and read data in RX RAM of `I2C_master`. After the software has finished reading, you can set `I2C_SLAVE_STRETCH_INT_CLR` (slave) to 1 to clear interrupt, and set `I2C_SLAVE_SCL_STRETCH_CLR` (slave) to release the SCL line.

16. After `I2C_master` has received the last byte of data, set `ack_value` (master) to 1. `I2C_slave` will stop the transfer once receiving the `I2C_NACK_INT` interrupt.

17. After data transfer completes, `I2C_master` executes the STOP command, and generates an `I2C_TRANS_COMPLETE_INT` (master) interrupt.
```