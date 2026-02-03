**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Table Header:**
- I2C_COMMAND2 (master)
- STOP

**Body Text with List Items and Descriptions:**

5. Write the address of I2Cslave and data to be sent to TX RAM of I2Cmaster in either FIFO mode or non-FIFO mode according to Section 27.4.10.

6. Write the address of I2Cslave to I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) register.

7. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.

8. Write 1 to I2C_TRANS_START (master) and I2CTrans_START (slave) to start transfer.

9. I2Cslave compares the slave address sent by I2Cmaster with its own address in I2C_SLAVE_ADDR (slave). When ack_check_en (master) in I2Cmaster’s WRITE command is 1, I2Cmaster checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2Cmaster does not check ACK value and take I2Cslave as a matching slave by default.

   - Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2Cmaster continues data transfer.
   
   - Not match: If the received ACK value does not match ack_exp, I2Cmaster generates an I2C_NACK_INT (master) interrupt and stops data transfer.

10. I2Cmaster sends data, and checks ACK value or not according to ack_check_en (master).

11. If data to be sent (N) is larger than 32 bytes, TX RAM of I2Cmaster may wrap around in FIFO mode. For details, please refer to Section 27.4.10.

12. If data to be received (N) is larger than 32 bytes, RX RAM of I2Cslave may wrap around in FIFO mode. For details, please refer to Section 27.4.10.

   - If data to be received (N) is larger than 32 bytes, the other way is to enable clock stretching by setting the I2C_SLAVE_SCL_STRETCH_EN (slave), and clearing I2C_RX_FULL_ACK_LEVEL. When RX RAM is full, an I2C_SLAVE_STRETCH_INT (slave) interrupt is generated. In this way, I2Cslave can hold SCL low, in exchange for more time to read data. After software has finished reading it, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.

13. After data transfer completes, I2Cmaster executes the STOP command, and generates an I2CTrans_COMPLETE_INT (master) interrupt.

**Subsection Title:**
27.5.2 I2Cmaster Writes to I2Cslave with a 10-bit Address in One Command Sequence

**Footer Information:**
Espressif Systems
998 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback