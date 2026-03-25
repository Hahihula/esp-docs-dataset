

```markdown
I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR 
(slave) to release the SCL line.

14. After data transfer completes, I2Cmaster executes the STOP command, and generates an 
I2C_TRANS_COMPLETE_INIT (master) interrupt.
```

## 30.5.4 I2Cmaster Writes to I2Cslave with a 7-bit Address in Multiple Command Sequences

### 30.5.4.1 Introduction

```markdown
Master cmd op_code byte_num
cmd0 RSTART
cmd1 WRITE N+1
cmd2 END

RAM addr0 (slave_addr<<1|r/w)
addr1 byte0
addr2 byte1
...
addrN byte(N-1)

Slave RAM addr0 byte0
addr1 byte1
addr2 ...
addrN-1 byte(N-1)

Segment0

Master cmd op_code byte_num
cmd0 WRITE M
cmd1 END/STOP

RAM addr0 byteN
addr1 byte(N+1)
addr2 byte(N+2)
...
addrM byte(M+N+1)

Slave RAM addr(N-1) byte(N-1)
addrN byteN
addr2 ...
addrM+N-1 byte(M+N-1)

Segment1

Master cmd op_code byte_num
cmd0 STOP

Segment2
```

Figure 30.5-4. I2Cmaster Writing to I2Cslave with a 7-bit Address in Multiple Sequences

Given that the I2C controller RAM holds only the size of TX/RX FIFO depth, when data are too large to be processed, it is advised to transmit them in multiple command sequences. At the end of every command sequence is an END command. When the controller executes this END command, SCL will be pulled low, and the software can refresh command sequence registers and the RAM for next transfer.

Figure 30.5-4 shows how I2Cmaster writes to an I2C slave in two or three segments as an example. For the first segment, the CMD_Controller registers are configured as shown in Segment0. Once data in I2Cmaster’s RAM is
```