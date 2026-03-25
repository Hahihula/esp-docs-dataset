

```markdown
14. I2Cslave sends data, and I2Cmaster checks ACK value or not according to ack_check_en (master) in the READ command.

15. If data to be read by I2Cmaster in one READ command (N or M) is larger than the TX FIFO depth of I2Cslave, an I2C_SLAVE_STRETCH_INT (slave) interrupt will be generated when TX RAM of I2Cslave becomes empty. In this way, I2Cslave can hold SCL low, so that software has more time to pad data in TX RAM of I2Cslave and read data in RX RAM of I2Cmaster. After the software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.

16. Once finishing reading data in the first READ command, I2Cmaster executes the END command and triggers an I2C_END_DETECT_INT (master) interrupt, which is cleared by setting I2C_END_DETECT_INT_CLR (master) to 1.

17. Update I2Cmaster’s command registers using one of the following two methods:

| Command registers of I2Cmaster | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|-------------------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMANDO (master)         | READ    | ack_value | ack_exp | 1            | M        |
| I2C_COMMAND1 (master)         | END     | —         | —       | —            | —        |

Or

| Command registers of I2Cmaster | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|-------------------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMANDO (master)         | READ    | 0         | 0       | 1            | M-1      |
| I2C_COMMANDO (master)         | READ    | 1         | 0       | 1            | 1        |
| I2C_COMMAND1 (master)         | STOP    | —         | —       | —            | —        |

18. Write M bytes of data to be sent to TX RAM of I2Cslave. If M is larger than the TX FIFO depth, then repeat step 12 in FIFO or non-FIFO mode.

19. Write 1 to I2C_TRANS_START (master) bit to start the transfer and repeat step 14.

20. If the last command is a STOP, then set ack_value (master) to 1 after I2Cmaster has received the last byte of data. I2Cslave stops transfer upon the I2C_NACK_INT interrupt. I2Cmaster executes the STOP command to stop the transfer and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.

21. If the last command is an END, then repeat step 16 and proceed to the next steps.

22. Update I2Cmaster’s command registers.

| Command registers of I2Cmaster | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|-------------------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMAND1 (master)         | STOP    | —         | —       | —            | —        |

23. Write 1 to I2C_TRANS_START (master) bit to start transfer.
```