

```markdown
sends a byte. When ack_check_en (master) is 0, I2Cmaster does not check the ACK value and take I2Cslave as a matching slave by default.

* Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2Cmaster continues data transfer.
* Not match: If the received ACK value does not match ack_exp, I2Cmaster generates an I2C_NACK_INT (master) interrupt and stops data transfer.

9. I2Cmaster sends data, and determines whether to check ACK value according to ack_check_en (master).

10. If data to be sent is larger than TX FIFO depth, TX RAM of I2Cmaster may wrap around in FIFO mode. For details, please refer to Section 27.4.10.

11. If data to be received is larger than RX FIFO depth, RX RAM of I2Cslave may wrap around in FIFO mode. For details, please refer to Section 27.4.10.

If data to be received is larger than RX FIFO depth, the other way is to enable clock stretching by setting I2C_SLAVE_SCL_STRETCH_EN (slave), and clearing I2C_RX_FULL_ACK_LEVEL to 0. When RX RAM is full, an I2C_SLAVE_STRETCH_INT (slave) interrupt is generated. In this way, I2Cslave can hold SCL low, in exchange for more time to read data. After the software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.

12. After data transfer completes, I2Cmaster executes the STOP command, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.
```

## 27.6.3 I2Cmaster Writes to I2Cslave with Two 7-bit Addresses in One Command Sequence

### 27.6.3.1 Introduction

![Figure 27.6-3. I2Cmaster Writing to I2Cslave with Two 7-bit Addresses](image_path_if_available)

**Figure 27.6-3. I2Cmaster Writing to I2Cslave with Two 7-bit Addresses**
```markdown
Master

cmd          op_code    byte_num
cmd0         RSTART     [blank]
cmd1         WRITE      N+2
cmd2         STOP       [blank]

RAM addr0 (slave_addr<<1|r/w)
addr1 M
addr2 byte0
addr(N+1) byte(N-1)

Slave

RAM addr0
... addrM
addr(M+1) byte0
addr(M+N) byte1
addr(M+N+1) byte(N-1)
```
```