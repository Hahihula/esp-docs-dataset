**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Section and Subsection Titles with Page Numbers:**
- GoBack

**Body Text:**

16. **I2C slave sends data, and I2C master checks ACK value or not according to ack_check_en (master) in the READ command.**

17. If data to be read by I2C master is larger than 32 bytes, an `I2C_SLAVE_STRETCH_INT` (slave) interrupt will be generated when TX RAM of I2C slave becomes empty. In this way, I2C slave can hold SCL low, so that software has more time to transmit data in TX RAM of I2C slave and read data in RX RAM of I2C master. After software has finished reading, you can set `I2C_SLAVE_STRETCH_INT_CLR` (slave) to 1 to clear interrupt, and set `I2C_SLAVE_SCL_STRETCH_CLR` (slave) to release the SCL line.

18. **After I2C master has received the last byte of data, set ack_value (master) to 1.** I2C slave will stop transfer once receiving the I2C_NACK_INT interrupt.
  
19. After data transfer complete, `I2C master` executes the STOP command and generates an `I2C_TRANS_COMPLETE_INIT` (master) interrupt.

**Subsection Title:**
27.5.7 **I2C master Reads I2C slave with Two 7-bit Address in One Command Sequence**

**Subsection Subtitle within Section:**
27.5.7.1 Introduction

**Figure Description and Caption:**
- Figure caption for the diagram:
  - "Figure 27.5-7 shows how I2C master reads data from specified addresses in an I2C slave."
  
**Diagram Details (from left to right, top to bottom):**

- **Master Table:** 
  - Columns labeled `cmd`, `op_code`, and `byte_num`.
  - Rows:
    - cmd0: RSTART
    - cmd1: WRITE with byte value "2"
    - cmd2: RSTART
    - cmd3: WRITE with byte value "1"
    - cmd4: READ N-1 (where 'N' is the number of bytes to read)
    - cmd5: READ 1

- **Slave Table:** 
  - Columns labeled `cmd`, `op_code`, and `byte_num`.
  - Rows:
    - cmd0: RSTART
    - cmd1: WRITE with byte value "2"
    - cmd2: RSTART
    - cmd3: WRITE with byte value "1"

- **RAM Table (slave):**
  - Columns labeled `addr0`, `addr1`, ..., `addr(N-1)`.
  - Rows:
    - addr0 to addr(N-1): byte values from 0 to N

**Figure Caption for the diagram below:**
- Figure caption with description of I2C master reading data in bytes, followed by a R/W bit indicating address again. The second byte is `I2C slave`'s memory address.

**Additional Text Below Diagram:**
- "Espressif Systems
  ESP32-S3 TRM (Version 1.7)
  Submit Documentation Feedback"