

```markdown
10. After the I2C_END_DETECT_INT (master) interrupt is generated, set I2C_END_DETECT_INT_CLR (master) to 1 to clear this interrupt.

11. Update I2Cmaster's command registers.

| Command registers | op_code   | ack_value | ack_exp | ack_check_er | byte_num |
|-------------------|-----------|-----------|---------|--------------|----------|
| I2C_COMMANDO      | WRITE     | ack_value | ack_exp | 1            | M        |
| (master)          |           |           |         |              |          |
| I2C_COMMAND1      | END/STOP   | —         | —       | —            | —        |
| (master)          |           |           |         |              |          |

12. Write M bytes of data to be sent to TX RAM of I2Cmaster in FIFO or non-FIFO mode.

13. Write 1 to I2C_TRANS_START (master) bit to start the transfer and repeat step 9.

14. If the command is a STOP, I2C stops the transfer and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.

15. If the command is an END, repeat step 10.

16. Update I2Cmaster's command registers.

| Command registers of I2Cmaster | op_code   | ack_value | ack_exp | ack_check_er | byte_num |
|---------------------------------|-----------|-----------|---------|--------------|----------|
| I2C_COMMAND1 (master)           | STOP      | —         | —       | —            | —        |

17. Write 1 to I2C_TRANS_START (master) to start transfer.

18. I2Cmaster executes the STOP command and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.
```

## 30.5.5 I2Cmaster Reads I2Cslave with a 7-bit Address in One Command Sequence