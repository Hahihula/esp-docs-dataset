

```markdown
| I2C_COMMAND0 (master) | RSTART | — | — | — | — |
|------------------------|--------|----:|-----:|-----:|-----:|
| I2C_COMMAND1 (master) | WRITE  |   0 |   0 |   1 |   2 |
| I2C_COMMAND2 (master) | RSTART | —  | —    | —    | —    |
| I2C_COMMAND3 (master) | WRITE  |   0 |   0 |   1 |   1 |
| I2C_COMMAND4 (master) | READ   |   0 |   0 |   1 | N-1  |
| I2C_COMMAND5 (master) | READ   |   1 |   0 |   1 |   1 |
| I2C_COMMAND6 (master) | STOP   | —  | —    | —    | —    |
```

5. Configure `I2C_SLAVE_ADDR` (slave) in `I2C_SLAVE_ADDR_REG` (slave) as `I2C_slave`'s 10-bit address, and set  
   `I2C_ADDR_10BIT_EN` (slave) to 1 to enable 10-bit addressing.

6. Write the address of `I2C_slave` to be sent to TX RAM of `I2C_master` in either FIFO or non-FIFO mode. The first byte of address comprises `(0x78 | I2C_SLAVE_ADDR[9:8])«1)` and a `R/W` bit, which is 1 and indicates a WRITE operation. The second byte of address is `I2C_SLAVE_ADDR[7:0]`. The third byte is `(0x78 | I2C_SLAVE_ADDR[9:8])«1)` and a `R/W` bit, which is 1 and indicates a READ operation.

7. Write 1 to `I2C_CONF_UPGATE` (master) and `I2C_CONF_UPGATE` (slave) to synchronize registers.

8. Write 1 to `I2C_TRANS_START` (master) to start `I2C_master`'s transfer.

9. Start `I2C_slave`'s transfer according to Section 30.4.14.

10. `I2C_slave` compares the slave address sent by `I2C_master` with its own address in `I2C_SLAVE_ADDR` (slave). When `ack_check_en` (master) in `I2C_master`'s WRITE command is 1, `I2C_master` checks ACK value each time it sends a byte. When `ack_check_en` (master) is 0, `I2C_master` does not check ACK value and takes `I2C_slave` as a matching slave by default.

    * Match: If the received ACK value matches `ack_exp` (master) (the expected ACK value), `I2C_master` continues data transfer.
    * Not match: If the received ACK value does not match `ack_exp`, `I2C_master` generates an `I2C_NACK_INT` (master) interrupt and stops data transfer.

11. `I2C_master` sends an RSTART and the third byte in TX RAM, which is `(0x78 | I2C_SLAVE_ADDR[9:8])«1)` and a `R/W` bit that indicates READ.

12. `I2C_slave` repeats step 10. If its address matches the address sent by `I2C_master`, `I2C_slave` proceed on to the next steps.

13. After `I2C_SLAVE_STRETCH_INT` (slave) is generated, the `I2C_STRETCH_CAUSE` bit is 0. The address of `I2C_slave` matches the address sent over SDA, and `I2C_slave` needs to send data.

14. Write data to be sent to TX RAM of `I2C_slave` in either FIFO mode or non-FIFO mode according to Section 30.4.10.

15. Set `I2C_SLAVE_SCL_STRETCH_CLR` (slave) to 1 to release SCL.
```