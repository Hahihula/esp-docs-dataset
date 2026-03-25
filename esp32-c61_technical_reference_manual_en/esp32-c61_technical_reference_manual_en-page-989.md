

```markdown
11. I2Cmaster sends a RSTART and the third byte in TX RAM, which is ((0x78 | I2C_SLAVE_ADDR[9:8])«1) and a R/W bit that indicates READ.
12. I2Cslave repeats step 10. If its address matches the address sent by I2Cmaster, I2Cslave proceed on to the next steps.
13. After I2C_SLAVE_STRETCH_INT (slave) is generated, the I2C_STRETCH_CAUSE bit is 0. The address of I2Cslave matches the address sent over SDA, and I2Cslave needs to send data.
14. Write data to be sent to TX RAM of I2Cslave in either FIFO mode or non-FIFO mode according to Section 27.4.10.
15. Set I2C_SLAVE_SCL_STRETCH_CLR (slave) to 1 to release SCL.
16. I2Cslave sends data, and I2Cmaster checks ACK value or not according to ack_check_en (master) in the READ command.
17. If data to be read by I2Cmaster is larger than the TX FIFO depth of I2Cslave, an I2C_SLAVE_STRETCH_INT (slave) interrupt will be generated when TX RAM of I2Cslave becomes empty. In this way, I2Cslave can hold SCL low, so that software has more time to pad data in TX RAM of I2Cslave and read data in RX RAM of I2Cmaster. After the software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.
18. After I2Cmaster has received the last byte of data, set ack_value (master) to 1. I2Cslave will stop transfer once receiving the I2C_NACK_INT interrupt.
19. After data transfer completes, I2Cmaster executes the STOP command, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.

## 27.6.7 I2Cmaster Reads I2Cslave with Two 7-bit Addresses in One Command Sequence
```