

```markdown
17. If data to be read by I2Cmaster is larger than the TX FIFO depth of I2Cslave, an I2C_SLAVE_STRETCH_INT (slave) interrupt will be generated when TX RAM of I2Cslave becomes empty. In this way, I2Cslave can hold SCL low, so that software has more time to pad data in TX RAM of I2Cslave and read data in RX RAM of I2Cmaster. After software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.

18. After I2Cmaster has received the last byte of data, set ack_value (master) to 1. I2Cslave will stop transfer once receiving the I2C_NACK_INT interrupt.

19. After data transfer completes, I2Cmaster executes the STOP command, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.
```

## 29.6.7 I2Cmaster Reads I2Cslave with Two 7-bit Addresses in One Command Sequence

### 29.6.7.1 Introduction

Figure 29.6-7 shows how I2Cmaster reads data from specified addresses in an I2C slave. I2Cmaster sends two bytes of addresses: the first byte is a 7-bit I2Cslave address followed by a R/W bit, which is 0 and indicates a WRITE; the second byte is I2Cslave’s memory address. After a RSTART condition, I2Cmaster sends the first byte of address again, but the R/W bit is 1 which indicates a READ. Then, I2Cmaster reads data starting from addrM.

**Figure 29.6-7. I2Cmaster Reading N Bytes of Data from addrM of I2Cslave with a 7-bit Address**

```markdown
Master

cmd | op_code | byte_num
----|---------|---------
cmd0| RSTART  |
cmd1| WRITE   | 2
cmd2| RSTART  |
cmd3| WRITE   | 1
cmd4| READ     | N-1
cmd5| READ     | 1
cmd6| STOP

RAM addr0 | (slave_addr<<1 | r/w) byte0
addr1    | M             | byte1
addr2    |               | byte2
...      | ...           |
addr(N-1)|               | byte(N-1)

Slave

RAM addr0 | ...
addrM     | byte0
addr(M+1) | byte1
addr(N+M-1)| byte(N-1)
```

```markdown
Espressif Systems 919 Submit Documentation Feedback ESP32-C6 TRM (Version 1.1)
```