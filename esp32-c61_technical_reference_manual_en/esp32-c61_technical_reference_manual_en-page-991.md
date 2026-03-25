

```markdown
| Command registers of I2Cmaster | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|---------------------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMANDO (master)          | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master)          | WRITE   | 0         | 0       | 1            | 2        |
| I2C_COMMAND2 (master)          | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND3 (master)          | WRITE   | 0         | 0       | 1            | 1        |
| I2C_COMMAND4 (master)          | READ    | 0         | 0       | 1            | N-1       |
| I2C_COMMAND5 (master)          | READ    | 1         | 0       | 1            | 1        |
| I2C_COMMAND6 (master)          | STOP    | —         | —       | —            | —        |

6. Configure I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) register as I2Cslave’s 7-bit address, and set I2C_ADDR_10BIT_EN (slave) to 0 to enable 7-bit addressing.
7. Write the address of I2Cslave and data to be sent to TX RAM of I2Cmaster in either FIFO or non-FIFO mode according to Section 27.4.10. The first byte of address comprises (I2C_SLAVE_ADDR[6:0])«1) and a R/W bit, which is 0 and indicates a WRITE. The second byte of the address is memory address M of I2Cslave. The third byte is (I2C_SLAVE_ADDR[6:0])«1) and a R/W bit, which is 1 and indicates a READ.
8. Write 1 to I2C_CONF_UPGA (master) and I2C_CONF_UPGA (slave) to synchronize registers.
9. Write 1 to I2C_TRANS_START (master) to start I2Cmaster’s transfer.
10. Start I2Cslave’s transfer according to Section 27.4.14.
11. I2Cslave compares the slave address sent by I2Cmaster with its own address in I2C_SLAVE_ADDR (slave). When ack_check_en (master) in I2Cmaster’s WRITE command is 1, I2Cmaster checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2Cmaster does not check ACK value and takes I2Cslave as a matching slave by default.
    * Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2Cmaster continues data transfer.
    * Not match: If the received ACK value does not match ack_exp, I2Cmaster generates an I2C_NACK_INT (master) interrupt and stops data transfer.
12. I2Cslave receives memory address sent by I2Cmaster and adds the offset.
13. I2Cmaster sends a RSTART and the third byte in TX RAM, which is ((0x78 | I2C_SLAVE_ADDR[6:0])«1)and an R bit.
14. I2Cslave repeats step 11. If its address matches the address sent by I2Cmaster, I2Cslave proceed on to the next steps.
15. Write data to be sent to TX RAM of I2Cslave in non-FIFO mode.
16. I2Cslave sends data, and I2Cmaster checks ACK value or not according to ack_check_en (master) in the READ command.
17. After I2Cmaster has received the last byte of data, set ack_value (master) to 1. I2Cslave will stop transfer once receiving the I2C_NACK_INT interrupt.
18. After data transfer completes, I2Cmaster executes the STOP command, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.
```