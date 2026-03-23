

```markdown
Chapter 28 I2C Controller (I2C)
GoBack

CMD_Controller registers, reloads the RAM and clears this interrupt, as shown in Segment1. If cmd1 in the second segment is a STOP, then data is transmitted to I2C_slave in two segments. I2C_master resumes data transfer after I2C_TRANS_START is set, and terminates the transfer by sending a STOP bit.

For the third segment, after the second data transfer finishes and an I2C_END_DETECT_INT is detected, the CMD_Controller registers of I2C_master are configured as shown in Segment2. Once I2C_TRANS_START is set, I2C_master generates a STOP bit and terminates the transfer.

Note that other I2C_masters will not transact on the bus between two segments. The bus is only released after a STOP signal is sent. The I2C controller can be reset by setting I2C_FSM_RST field at any time. This field will later be cleared automatically by hardware.

28.5.4.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
3. Configure command registers of I2C_master.

| Command registers | op_code | ack_value | ack_exp | ack_check_er | byte_num |
|:------------------|:---------|:-----------|:---------|:--------------|:----------|
| I2C_COMMANDO (master) | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master) | WRITE   | ack_value | ack_exp | 1            | N+1       |
| I2C_COMMAND2 (master) | END     | —         | —       | —            | —        |

4. Write I2C_slave address and data to be sent to TX RAM of I2C_master in either FIFO mode or non-FIFO mode according to Section 28.4.10.
5. Write address of I2C_slave to I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) register
6. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
7. Write 1 to I2C_TRANS_START (master) and I2C_TRANS_START (slave) to start transfer.
8. I2C_slave compares the slave address sent by I2C_master with its own address in I2C_SLAVE_ADDR (slave). When ack_check_en (master) in I2C_master’s WRITE command is 1, I2C_master checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2C_master does not check ACK value and take I2C_slave as matching slave by default.

* Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2C_master continues data transfer.
* Not match: If the received ACK value does not match ack_exp, I2C_master generates an I2C_NACK_INT (master) interrupt and stops data transfer.

9. I2C_master sends data, and checks ACK value or not according to ack_check_en (master).
10. After the I2C_END_DETECT_INT (master) interrupt is generated, set I2C_END_DETECT_INT_CLR (master) to 1 to clear this interrupt.
11. Update I2C_master’s command registers.

Espressif Systems
695
ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback
```