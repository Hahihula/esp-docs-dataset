**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Body Text with Instructions and Descriptions:**

10. After the `I2C_END_DETECT_INT` (master) interrupt is generated, set `I2CEND_DETECT_INT_CLR` (master) to 1 to clear this interrupt.

11. Update I2C master’s command registers:

| Command registers | op_code | ack_value | ack_exp | ack_check_err | byte_num |
|--------------------|---------|-----------|---------|---------------|----------|
| `I2C_COMMANDO`    | (master) WRITE | —       | 1      | M             |          |
| `I2C_COMMAND1`     | (master) END/STOP | —        | —      | —             |          |

12. Write \(M\) bytes of data to be sent to TX RAM of I2C master in FIFO or non-FIFO mode.

13. Write 1 to `I2CTransStart` (master) bit to start transfer and repeat step 9.

14. If the command is a STOP, I2C stops transfer and generates an `I2CTransComplete_INT` (master) interrupt.

15. If the command is an END, repeat step 10.

16. Update I2C master’s command registers:

| Command registers | op_code | ack_value | ack_exp | ack_check_err | byte_num |
|--------------------|---------|-----------|---------|---------------|----------|
| `I2C_COMMAND1`     | (master) STOP | —        | —      | —             |          |

17. Write 1 to `I2CTransStart` (master) bit to start transfer.

18. I2C master executes the STOP command and generates an `I2CTransComplete_INT` (master) interrupt.

**Highlighted Section:**
- **Subtitle:** Read I2C slave with a 7-bit Address in One Command Sequence

**Footer Information:**
- Page Number: 1004
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name and Link for Feedback:
  - Espressif Systems
  - Submit Documentation Feedback