**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Section Header:**
8. I2CSlave compares the slave address sent by I2Cmaster with its own address in I2C_SLAVE_ADDR (slave).

**Body Text:**
When ack_check_en (master) in I2Cmaster’s WRITE command is 1, I2Cmaster checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2Cmaster does not check ACK value and take I2Cslave as matching slave by default.

- **Subsection:**
  - Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2Cmaster continues data transfer.
  
- **Subsection:**
  - Not match: If the received ACK value does not match ack_exp, I2Cmaster generates an I2C_NACK_INT (master) interrupt and stops data transfer.

**Section Header:**
9. I2Cmaster sends data, and checks ACK value or not according to ack_check_en (master).

**Body Text:**
10. If data to be sent is larger than 32 bytes, TX RAM of I2Cmaster may wrap around in FIFO mode. For details, please refer to Section **27.4.10**.

11. If data to be received is larger than 32 bytes, RX RAM of I2Cslave may wrap up around in FIFO mode. For details, please refer to Section **27.4.10**.

If data to be received is larger than 32 bytes, the other way is to enable clock stretching by setting I2C_SLAVE_SCL_STRETCH_EN (slave), and clearing I2C_RX_FULL_ACK_LEVEL to O. When RX RAM is full, an I2C_SLAVE_STRETCH_INT (slave) interrupt is generated. In this way, I2Cslave can hold SCL low, in exchange for more time to read data. After software has finished reading it, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.

**Section Header:**
12. After data transfer completes, I2Cmaster executes the STOP command, and generates an I2C_TRANSComplete_INIT (master) interrupt.

**Subsection Title:**
27.5.3 I2Cmaster Writes to I2Cslave with Two 7-bit Addresses in One Command Sequence

**Subsection Header:**
27.5.3.1 Introduction

**Diagram Description and Caption:**
- **Figure:** Figure 27.5-3, "I2Cmaster Writing to I2Cslave with Two 7-bit Addresses"
  
  - The diagram shows a sequence of commands (cmd) from the master side including op_code and byte_num for different operations like RSTART, WRITE, N+2, STOP.
  - It also illustrates SCL communication between Master and Slave over RAM addresses (addr0 to addr(N-1)).

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback