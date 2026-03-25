

```markdown
16. I2Cslave sends data, and I2Cmaster checks ACK value or not according to ack_check_en (master) in the READ command.

17. If data to be read by I2Cmaster is larger than the TX FIFO depth of I2Cslave, an I2C_SLAVE_STRETCH_INT (slave) interrupt will be generated when TX RAM of I2Cslave becomes empty. In this way, I2Cslave can hold SCL low, so that software has more time to pad data in TX RAM of I2Cslave and read data in RX RAM of I2Cmaster. After the software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.

18. After I2Cmaster has received the last byte of data, set ack_value (master) to 1. I2Cslave will stop the transfer once receiving the I2C_NACK_INT interrupt.

19. After data transfer completes, I2Cmaster executes the STOP command, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.
```

### 30.5.7 I2Cmaster Reads I2Cslave with Two 7-bit Addresses in One Command Sequence

#### 30.5.7.1 Introduction

![Figure 30.5-7](image_reference)

**Figure 30.5-7. I2Cmaster Reading N Bytes of Data from addrM of I2Cslave with a 7-bit Address**

> Figure 30.5-7 shows how I2Cmaster reads data from specified addresses in an I2C slave. I2Cmaster sends two bytes of addresses: the first byte is a 7-bit I2Cslave address followed by a R/W bit, which is 0 and indicates a WRITE; the second byte is I2Cslave’s memory address. After an RSTART condition, I2Cmaster sends the first byte of address again, but the R/W bit is 1 which indicates a READ. Then, I2Cmaster reads data starting from addrM.
```