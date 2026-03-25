
```markdown
14. If the command is a STOP, I2C stops the transfer and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.
15. If the command is an END, repeat step 10.
16. Update I2Cmaster's command registers.

| Command registers of I2Cmaster | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|---------------------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMAND1 (master)           | STOP    | —         | —       | —            | —        |

17. Write 1 to I2C_TRANS_START (master) bit to start transfer.
18. I2Cmaster executes the STOP command and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.

### 34.7.5 I2Cmaster Reads I2Cslave with a 7-bit Address in One Command Sequence

#### 34.7.5.1 Introduction

**Figure 34.7-5. I2Cmaster Reading I2Cslave with a 7-bit Address**

Master
```
cmd | op_code   | byte_num |
-----|-----------|----------|
cmd0 | RSTART    |          |
cmd1 | WRITE     | 1        |
cmd2 | READ      | N-1      |
cmd3 | READ      | 1        |
cmd4 | STOP      |          |

RAM
addr0 | (slave_addr<<1) r/w byte0
addr1 | byte1
addr2 | byte2
...
addr(N-1)| byte(N-1)
```

Slave
```
RAM
addr0 | byte0
addr1 | byte1
addr2 | ...
addr(N-1)| byte(N-1)
```

Figure 34.7-5 shows how I2Cmaster reads N bytes of data from an I2C slave using 7-bit addressing. cmd1 is a WRITE command, and when this command is executed I2Cmaster sends the address of I2Cslave. The byte sent comprises a 7-bit I2Cslave address and a R/W bit. When the R/W bit is 1, it indicates a READ operation. If the address of an I2C slave matches the sent address, this matching slave starts sending data to I2Cmaster. I2Cmaster generates acknowledgments according to ack_value defined in the READ command upon receiving a byte.

As illustrated in Figure 34.7-5, I2Cmaster executes two READ commands: it generates ACKs for (N-1) bytes of data in cmd2, and a NACK for the last byte of data in cmd 3. This configuration may be changed as required.
```