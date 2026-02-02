**Title:**
Chapter 21 I2C Controller (I2C)

**Subtitle:**
Register 21.21. I2C_COMMAND_REG (n : 0-15) (0x58+4*n)

**Binary Diagram Description:**
The diagram shows a binary representation of the register with labels for specific bits:
- "31" to "0": These are labeled as reserved.
- The bit positions from rightmost side, starting at position n=0 up to 2n (where 'n' ranges from 0 through 15).

**Text Explanation:**
I2C_COMMANDDONE When command n is done in I2C Master mode, this bit changes to high level. (R/W)

I2C_COMMAND This is the content of command n. It consists of three parts: (R/W)
- op_code is the command code.
  - RSTART
  - WRITE
  - READ
  - STOP
  - END

Byte_num represents the number of bytes that need to be sent or received.

ack_check_en, ack_exp and ack are used to control the ACK bit. See I2C cmd structure for more information.

**Footer:**
Espressif Systems  
414 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback