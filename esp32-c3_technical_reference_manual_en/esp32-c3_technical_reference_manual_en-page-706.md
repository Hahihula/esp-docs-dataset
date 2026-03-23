

```markdown
13. Set I2C_SLAVE_SCL_STRETCH_CLR (slave) to 1 to release SCL.

14. I2C<sub>slave</sub> sends data, and I2C<sub>master</sub> checks ACK value or not according to ack_check_en (master) in the READ command.

15. If data to be read by I2C<sub>master</sub> in one READ command (N or M) is larger than 32 bytes, an I2C_SLAVE_STRETCH_INT (slave) interrupt will be generated when TX RAM of I2C<sub>slave</sub> becomes empty. In this way, I2C<sub>slave</sub> can hold SCL low, so that software has more time to pad data in TX RAM of I2C<sub>slave</sub> and read data in RX RAM of I2C<sub>master</sub>. After software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.

16. Once finishing reading data in the first READ command, I2C<sub>master</sub> executes the END command and triggers an I2C_END_DETECT_INT (master) interrupt, which is cleared by setting I2C_END_DETECT_INT_CLR (master) to 1.

17. Update I2C<sub>master</sub>'s command registers using one of the following two methods:

| Command registers          | op_code | ack_value   | ack_exp | ack_check_er | byte_num |
|----------------------------|---------|-------------|---------|--------------|----------|
| I2C_COMMANDO (master)      | READ    | ack_value   | ack_exp | 1            | M        |
| I2C_COMMAND1 (master)      | END     | —           | —       | —            | —        |

Or

| Command registers          | op_code | ack_value | ack_exp | ack_check_er | byte_num |
|----------------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMANDO (master)      | READ    | 0         | 0       | 1            | M-1      |
| I2C_COMMANDO (master)      | READ    | 1         | 0       | 1            | 1        |
| I2C_COMMAND1 (master)      | STOP    | —         | —       | —            | —        |

18. Write M bytes of data to be sent to TX RAM of I2C<sub>slave</sub>. If M is larger than 32, then repeat step 14 in FIFO or non-FIFO mode.

19. Write 1 to I2C_TRANS_START (master) bit to start transfer and repeat step 14.

20. If the last command is a STOP, then set ack_value (master) to 1 after I2C<sub>master</sub> has received the last byte of data. I2C<sub>slave</sub> stops transfer upon the I2C_NACK_INT interrupt. I2C<sub>master</sub> executes the STOP command to stop transfer and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.

21. If the last command is an END, then repeat step 16 and proceed on to the next steps.

22. Update I2C<sub>master</sub>'s command registers.

| Command registers          | op_code | ack_value | ack_exp | ack_check_er | byte_num |
|----------------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMAND1 (master)      | STOP    | —         | —       | —            | —        |

23. Write 1 to I2C_TRANS_START (master) bit to start transfer.

24. I2C<sub>master</sub> executes the STOP command to stop transfer, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.
```