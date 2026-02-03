**Chapter 27 I²C Controller (I2C)**

---

| **I²C COMMAND** | **(master)** | **(slave) ——** |
| --- | --- | --- |
| I2C_COMMAND0 | RSTART | — |
| I2C_COMMAND1 | WRITE | O | 1 | 1 |
| I2C_COMMAND2 | READ | O | 0 | N-1 |
| I2C_COMMAND3 | READ | 1 | 0 | 1 |
| I2C_COMMAND4 | STOP | — | — | |

5. Write the address of `I²C_slave` to TX RAM of `I²C_master` in either FIFO mode or non-FIFO mode according to Section **27.4.10**.

6. Write the address of `I²C_slave` to `I²C_SLAVE_ADDR` (slave) in `I²C_SLAVE_ADDR_REG` (slave) register.

7. Write 1 to `I²C_CONF_UPGRADE` (master) and `I²C_CONF_UPDATE` (slave) to synchronize registers.

8. Write 1 to `I²CTrans_START` (master) bit to start `I²C_master`’s transfer.

9. Start `I²C_slave`’s transfer according to Section **27.4.14**.

10. `I²C_slave` compares the slave address sent by `I²C_master` with its own address in `I²C_SLAVE_ADDR` (slave). When `ack_check_en` (master) in `I²C_master`’s WRITE command is 1, `I²C_master` checks ACK value each time it sends a byte. When `ack_check_en` (master) is 0, `I²C_master` does not check ACK value and take `I²C_slave` as matching slave by default.

    - **Match:** If the received ACK value matches `ack_exp` (master) (the expected ACK value), `I²C_master` continues data transfer.
    
    - **Not match:** If the received ACK value does not match `ack_exp`, `I²C_master` generates an `I²C_NACK_INT` (master) interrupt and stops data transfer.

11. After `I²C_SLAVE_STRETCH_INT` (slave) is generated, the `I²C.Stretch_CAUSE` bit is 0. The address of `I²C_slave` matches the address sent over SDA, and `I²C_slave` needs to send data.

12. Write data to be sent to TX RAM of `I²C_slave` in either FIFO mode or non-FIFO mode according to Section **27.4.10**.

13. Set `I²C_SLAVE_STRETCH_CLR` (slave) to 1 to release `SCL`.

14. `I²CSlave` sends data, and `I²C_master` checks ACK value or not according to `ack_check_en` (master) in the READ command.

15. If data to be read by `I²C_master` is larger than 32 bytes, an `I²C_SLAVE_STRETCH_INT` (slave) interrupt will be generated when TX RAM of `I²C_slave` becomes empty. In this way, `I²CSlave` can hold SCL low so that software has more time to pad data in TX RAM of `I²C_slave` and read data in RX RAM of `I²C_master`. After software has finished reading, you can set `I²C_SLAVE_STRETCH_INT_CLR` (slave) to 1 to clear interrupt, and set `I²C_SLAVE_SCL_STRETCH_CLR` (slave) to release the SCL line.

16. After `I²C_master` has received the last byte of data, set `ack_value` (master) to 1. `I²CSlave` will stop transfer once receiving the `I²C_NACK_INT` interrupt.

17. After data transfer completes, `I²C_master` executes the STOP command and generates an `I²C_TRANS_COMPLETE_IN` (master) interrupt.

---

**Espressif Systems**

**ESP32-S3 TRM (Version 1.7)**

**Submit Documentation Feedback**