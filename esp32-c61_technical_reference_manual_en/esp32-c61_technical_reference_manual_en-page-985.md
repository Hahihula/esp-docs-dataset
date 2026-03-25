

```markdown
| I2C_COMMAND1 (master) | END/STOP | — | — | — |
|------------------------|----------|---|---|---|

12. Write M bytes of data to be sent to TX RAM of I2Cmaster in FIFO or non-FIFO mode.
13. Write 1 to I2C_TRANS_START (master) bit to start the transfer and repeat step 9.
14. If the command is a STOP, I2C stops the transfer and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.
15. If the command is an END, repeat step 10.
16. Update I2Cmaster’s command registers.

Command registers of I2Cmaster
| I2C_COMMAND1 (master) | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|------------------------|---------|-----------|---------|--------------|----------|
|                        | STOP    | —         | —       | —            | —        |

17. Write 1 to I2C_TRANS_START (master) bit to start transfer.
18. I2Cmaster executes the STOP command and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.

## 27.6.5 I2Cmaster Reads I2Cslave with a 7-bit Address in One Command Sequence

### 27.6.5.1 Introduction

Figure 27.6-5 shows how I2Cmaster reads N bytes of data from an I2C slave using 7-bit addressing. cmd1 is a WRITE command, and when this command is executed I2Cmaster sends the address of I2Cslave. The byte sent comprises a 7-bit I2Cslave addresses and a R/W bit. When the R/W bit is 1, it indicates a READ operation. If the
```