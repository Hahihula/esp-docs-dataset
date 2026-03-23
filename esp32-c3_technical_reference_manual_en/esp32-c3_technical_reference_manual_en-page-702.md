

```markdown
| I2C_COMMAND2 (master) | RSTART | — | — | — | — |
|------------------------|--------|----|----|----|----|
| I2C_COMMAND3 (master) | WRITE  | 0  | 0  | 1  | 1  |
| I2C_COMMAND4 (master) | READ   | 0  | 0  | 1  | N-1|
| I2C_COMMAND5 (master) | READ   | 1  | 0  | 1  | 1  |
| I2C_COMMAND6 (master) | STOP   | —  | —  | —  | —  |

6. Configure `I2C_SLAVE_ADDR` (slave) in `I2C_SLAVE_ADDR_REG` (slave) register as `I2C_slave`’s 7-bit address, and set `I2C_ADDR_10BIT_EN` (slave) to 0 to enable 7-bit addressing.
7. Write `I2C_slave` address and data to be sent to TX RAM of `I2C_master` in either FIFO or non-FIFO mode according to Section 28.4.10. The first byte of address comprises (`I2C_SLAVE_ADDR[6:0]`) «1» and a R/W bit, which is 0 and indicates a WRITE. The second byte of address is memory address M of `I2C_slave`. The third byte is (`I2C_SLAVE_ADDR[6:0]`) «1» and a R/W bit, which is 1 and indicates a READ.
8. Write 1 to `I2C_CONF_UPGATE` (master) and `I2C_CONF_UPGATE` (slave) to synchronize registers.
9. Write 1 to `I2C_TRANS_START` (master) and `I2C_TRANS_START` (slave) to start `I2C_master`’s transfer.
10. Start `I2C_slave`’s transfer according to Section 28.4.14.
11. `I2C_slave` compares the slave address sent by `I2C_master` with its own address in `I2C_SLAVE_ADDR` (slave). When `ack_check_en` (master) in `I2C_master`’s WRITE command is 1, `I2C_master` checks ACK value each time it sends a byte. When `ack_check_en` (master) is 0, `I2C_master` does not check ACK value and take `I2C_slave` as matching slave by default.
    * Match: If the received ACK value matches `ack_exp` (master) (the expected ACK value), `I2C_master` continues data transfer.
    * Not match: If the received ACK value does not match `ack_exp`, `I2C_master` generates an `I2C_NACK_INT` (master) interrupt and stops data transfer.
12. `I2C_slave` receives memory address sent by `I2C_master` and adds the offset.
13. `I2C_master` sends a RSTART and the third byte in TX RAM, which is (`(0x78 | I2C_SLAVE_ADDR[9:8])`) «1» and a R bit.
14. `I2C_slave` repeats step 11. If its address matches the address sent by `I2C_master`, `I2C_slave` proceed on to the next steps.
15. After `I2C_SLAVE_STRETCH_INT` (slave) is generated, the `I2C_STRETCH_CAUSE` bit is 0. The `I2C_slave` address matches the address sent over SDA, and `I2C_slave` needs to send data.
16. Write data to be sent to TX RAM of `I2C_slave` in either FIFO mode or non-FIFO mode according to Section 28.4.10.
17. Set `I2C_SLAVE_SCL_STRETCH_CLR` (slave) to 1 to release SCL.
18. `I2C_slave` sends data, and `I2C_master` checks ACK value or not according to `ack_check_en` (master) in the READ command.
```