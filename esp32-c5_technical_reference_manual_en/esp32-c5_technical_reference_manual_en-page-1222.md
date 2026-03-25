

```markdown
2. We recommend setting I2C_SLAVE_SCL_STRETCH_EN (slave) to 1, so that SCL can be held low for more processing time when I2C<sub>slave</sub> needs to send data. If this bit is not set, the software should write data to be sent to I2C<sub>slave</sub>'s TX RAM before I2C<sub>master</sub> initiates the transfer. The configuration below is applicable to a scenario where I2C_SLAVE_SCL_STRETCH_EN (slave) is 1.

3. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.

4. Configure command registers of I2C<sub>master</sub>.

| Command registers of I2C<sub>master</sub> | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|------------------------------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMAND0 (master)                   | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master)                   | WRITE   | 0         | 0       | 1            | 2        |
| I2C_COMMAND2 (master)                   | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND3 (master)                   | WRITE   | 0         | 0       | 1            | 1        |
| I2C_COMMAND4 (master)                   | READ    | 0         | 0       | 1            | N-1      |
| I2C_COMMAND5 (master)                   | READ    | 1         | 0       | 1            | 1        |
| I2C_COMMAND6 (master)                   | STOP    | —         | —       | —            | —        |

5. Configure I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) as I2C<sub>slave</sub>'s 10-bit address, and set I2C_ADDR_10BIT_EN (slave) to 1 to enable 10-bit addressing.

6. Write the address of I2C<sub>slave</sub> and data to be sent to TX RAM of I2C<sub>master</sub> in either FIFO or non-FIFO mode. The first byte of address comprises ((0x78 | I2C_SLAVE_ADDR[9:8])«1) and a R/W bit, which is 1 and indicates a WRITE operation. The second byte of address is I2C_SLAVE_ADDR[7:0]. The third byte is ((0x78 | I2C_SLAVE_ADDR[9:8])«1) and a R/W bit, which is 1 and indicates a READ operation.

7. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.

8. Write 1 to I2C_TRANS_START (master) to start I2C<sub>master</sub>'s transfer.

9. Start I2C<sub>slave</sub>'s transfer according to Section 34.4.14.

10. I2C<sub>slave</sub> compares the slave address sent by I2C<sub>master</sub> with its own address in I2C_SLAVE_ADDR (slave). When ack_check_en (master) in I2C<sub>master</sub>'s WRITE command is 1, I2C<sub>master</sub> checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2C<sub>master</sub> does not check ACK value and take I2C<sub>slave</sub> as a matching slave by default.
    * Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2C<sub>master</sub> continues data transfer.
    * Not match: If the received ACK value does not match ack_exp, I2C<sub>master</sub> generates an I2C_NACK_INT (master) interrupt and stops data transfer.

11. I2C<sub>master</sub> sends a RSTART and the third byte in TX RAM, which is ((0x78 | I2C_SLAVE_ADDR[9:8])«1) and a R/W bit that indicates READ.

12. I2C<sub>slave</sub> repeats step 10. If its address matches the address sent by I2C<sub>master</sub>, I2C<sub>slave</sub> proceed on to the next steps.

13. After I2C_SLAVE_STRETCH_INT (slave) is generated, the I2C_STRETCH_CAUSE bit is 0. The address of I2C<sub>slave</sub> matches the address sent over SDA, and I2C<sub>slave</sub> needs to send data.
```