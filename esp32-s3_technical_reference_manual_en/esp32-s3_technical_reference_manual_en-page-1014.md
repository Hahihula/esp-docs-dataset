**Chapter 27 I²C Controller (I2C)**

---

### Section: Command and Register Operations for I²C Master

14. **I²C slave sends data, and I²C master checks ACK value or not according to ack_check_en (master) in the READ command.**

15. If data to be read by `I2C_master` in one READ command (N or M) is larger than 32 bytes, an `I2C_SLAVE_STRETCH_INT` (slave) interrupt will be generated when TX RAM of `I2C_slave` becomes empty.
   - In this way, `I2C_slave` can hold SCL low so that software has more time to read pad data in TX RAM of `I2C_slave` and read data in RX RAM of `I2C_master`.
   - After software has finished reading, you can set `I2C_SLAVE_STRETCH_INT` (slave) to 1 to clear interrupt, and set `I2C_SLAVE_SCL_STRETCH_CLR` (slave) to release the SCL line.

16. Once finishing reading data in the first READ command, `I2C_master` executes the END command and triggers an I²C_END_DETECT_INT (master) interrupt, which is cleared by setting `I2C_END_DETECT_INTCLR` (master) to 1.

17. **Update I²C master’s command registers using one of the following two methods:**

| Command | registers of op_code | ack value | ack_exp | ack_check_err | byte_num |
|---------|-----------------------|----------|--------|---------------|----------|
| `I2C_COMMAND` (master) | READ | —       | 1      | M             |          |
| `I2C_COMMAND1` (master) | END | —       | —      | —             |          |

**OR**

| Command | registers of op_code | ack_value | ack_exp | ack_check_err | byte_num |
|---------|-----------------------|----------|--------|---------------|----------|
| `I2C_COMMAND` (master) | READ | 0        | 0      | 1             | M-1      |
| `I2C_COMMAND` (master) | READ | 1        | 0      | 1             | 1        |
| `I2C_COMMAND1` (master) | STOP | —       | —      | —             |          |

18. **Write M bytes of data to be sent to TX RAM of I²C slave. If M is larger than 32, then repeat step 14 in FIFO or non-FIFO mode.**

19. Write 1 to `I2CTransStart` (master) bit to start transfer and repeat step 14.

20. **If the last command is a STOP, then set ack_value (master) to 1 after I²C master has received the last byte of data.**
   - `I2C_slave` stops transfer upon the I²C_NACK_INT interrupt.
   - `I2C_master` executes the STOP command to stop transfer and generates an I²C_TRANSComplete_INT (master) interrupt.

21. If the last command is an END, then repeat step 16 and proceed on to the next steps.

22. **Update I²C master’s command registers:**

| Command | registers of op_code | ack_value | ack_exp | ack_check_err | byte_num |
|---------|-----------------------|----------|--------|---------------|----------|
| `I2C_COMMAND1` (master) | STOP | —       | —      | —             |          |

23. Write 1 to `I2CTransStart` (master) bit to start transfer.

---

**Footer:**
- Espressif Systems
- Document Version Information:
  - Document ID: 1014
  - Document Title: ESP32-S3 TRM (Version 1.7)
  - Submit Documentation Feedback