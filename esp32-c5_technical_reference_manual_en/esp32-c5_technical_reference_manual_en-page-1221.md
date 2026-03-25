

```markdown
15. If data to be read by I2Cmaster is larger than the TX FIFO depth of I2Cslave, an I2C_SLAVE_STRETCH_INT (slave) interrupt will be generated when TX RAM of I2Cslave becomes empty. In this way, I2Cslave can hold SCL low, so that software has more time to pad data in TX RAM of I2Cslave and read data in RX RAM of I2Cmaster. After software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.

16. After I2Cmaster has received the last byte of data, set ack_value (master) to 1. I2Cslave will stop the transfer once receiving the I2C_NACK_INT interrupt.

17. After data transfer completes, I2Cmaster executes the STOP command, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.
```

### 34.7.6 I2Cmaster Reads I2Cslave with a 10-bit Address in One Command Sequence

#### 34.7.6.1 Introduction

![Figure 34.7-6: I2Cmaster Reading I2Cslave with a 10-bit Address](image_reference)

**Figure 34.7-6. I2Cmaster Reading I2Cslave with a 10-bit Address**

Figure 34.7-6 shows how I2Cmaster reads data from an I2C slave using 10-bit addressing. Unlike 7-bit addressing, in 10-bit addressing the WRITE command of the I2Cmaster is formed from two bytes, and correspondingly TX RAM of this master stores a 10-bit address of two bytes. The R/W bit in the first byte is 0, which indicates a WRITE operation. After a RSTART condition, I2Cmaster sends the first byte of address again to read data from I2Cslave, but the R/W bit is 1, which indicates a READ operation. The two address bytes can be configured as described in Section 34.7.2.

#### 34.7.6.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
```