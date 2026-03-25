

```markdown
| Command registers | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|:-------------------|:---------|:-----------|:---------|:--------------|:----------|
| I2C_COMMANDO (master) | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master) | WRITE   | —         | ack_exp | 1             | N+1       |
| I2C_COMMAND2 (master) | END     | —         | —       | —            | —        |

4. Write the address of I2C<sub>slave</sub> and data to be sent to TX RAM of I2C<sub>master</sub> in either FIFO mode or non-FIFO mode according to Section 27.4.10.
5. Write the address of I2C<sub>slave</sub> to I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) register.
6. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
7. Write 1 to I2C_TRANS_START (master) and I2C_TRANS_START (slave) to start transfer.
8. I2C<sub>slave</sub> compares the slave address sent by I2C<sub>master</sub> with its own address in I2C_SLAVE_ADDR (slave).
   When ack_check_en (master) in I2C<sub>master</sub>'s WRITE command is 1, I2C<sub>master</sub> checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2C<sub>master</sub> does not check ACK value and take I2C<sub>slave</sub> as a matching slave by default.
   * Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2C<sub>master</sub> continues data transfer.
   * Not match: If the received ACK value does not match ack_exp, I2C<sub>master</sub> generates an I2C_NACK_INT (master) interrupt and stops data transfer.
9. I2C<sub>master</sub> sends data, and checks ACK value or not according to ack_check_en (master).
10. After the I2C_END_DETECT_INT (master) interrupt is generated, set I2C_END_DETECT_INT_CLR (master) to 1 to clear this interrupt.
11. Update I2C<sub>master</sub>'s command registers.

| Command registers | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|:-------------------|:---------|:-----------|:---------|:--------------|:----------|
| I2C_COMMANDO (master) | WRITE   | —         | ack_exp | 1             | M         |
```