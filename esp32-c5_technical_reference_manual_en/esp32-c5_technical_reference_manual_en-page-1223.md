

```markdown
14. Write data to be sent to TX RAM of I2Cslave in either FIFO mode or non-FIFO mode according to Section 34.4.10.
15. Set I2C_SLAVE_SCL_STRETCH_CLR (slave) to 1 to release SCL.
16. I2Cslave sends data, and ICmaster checks ACK value or not according to ack_check_en (master) in the READ command.
17. If data to be read by ICmaster is larger than the TX FIFO depth of I2Cslave, an I2C_SLAVE_STRETCH_INT (slave) interrupt will be generated when TX RAM of I2Cslave becomes empty. In this way, I2Cslave can hold SCL low, so that software has more time to pad data in TX RAM of I2Cslave and read data in RX RAM of ICmaster. After the software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.
18. After ICmaster has received the last byte of data, set ack_value (master) to 1. I2Cslave will stop transfer once receiving the I2C_NACK_INT interrupt.
19. After data transfer completes, ICmaster executes the STOP command, and generates an I2C_TRANS_COMPLETE_INIT (master) interrupt.

34.7.7 I2Cmaster Reads I2Cslave with Two 7-bit Addresses in One Command Sequence

34.7.7.1 Introduction
```

![Figure 34.7-7](image_description)

**Figure 34.7-7. I2Cmaster Reading N Bytes of Data from addrM of I2Cslave with a 7-bit Address**

> Figure 34.7-7 shows how ICmaster reads data from specified addresses in an I2C slave. ICmaster sends two bytes of addresses: the first byte is a 7-bit I2Cslave address followed by a R/W bit, which is 0 and indicates a
```