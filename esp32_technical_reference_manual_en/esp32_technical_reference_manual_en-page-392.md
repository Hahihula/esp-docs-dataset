**Chapter Title:**
Chapter 21 I2C Controller (I2C)

**Body Text:**

Figure **21.3-3** also shows the registers that can configure the START bit, STOP bit, SDA hold time, and SDA sample time.

**Notice:** If the I2C pads are configured in open-drain mode, it will take longer for the signal lines to transition from a low level to a high level. The transition duration is determined together by the pull-up resistor and capacitor. The output frequency of SCL is relatively low in open-drain mode.

**Subtitle:**
21.3.4 I2C cmd Structure

**Image Description (Figure 21.3-4):**
Structure Of The I2C Command Register
```
cmd0 | op_code | ack_value | ack_exp | ack_check_en | byte_num
     +-------+---------+--------+-----------+----------+
    31    |   ...  |    10   |    9    |      8    |    7:0  
```

**Body Text Continued:**

The Command register is active only in I2C master mode, with its internal structure shown in Figure **21.3-4**.

CMD_DONE: The CMDDone bit of every command can be read by software to tell if the command has been handled by hardware.
op_code: op_code is used to indicate the command. The I2C controller supports four commands:
- RSTART: op_code = 0 is the RSTART command to control the transmission of a START or RESTART I2C condition.
- WRITE: op_code = 1 is the WRITE command for the I2C Master to transmit data.
- READ: op_code = 2 is the READ command for the I2C Master to receive data.
- STOP: op_code = 3 is the STOP command to control the transmission of a STOP I2C condition.

END: op_code = 4 is the END command for continuous data transmission. When the END command is given, SCL is temporarily disabled to allow software to reload the command and data registers for subsequent events before resuming. Transmission will then continue seamlessly.
A complete data transmission process begins with an RSTART command, and ends with a STOP command.

ack_value: When receiving data, this bit is used to indicate whether the receiver will send an ACK after this byte has been received.
ack_exp: This bit is to set an expected ACK value for the transmitter.
ack_check_en: When transmitting a byte, this bit enables checking the ACK value received against the ack_exp value. Checking is enabled by 1, while 0 disables it.

byte_num: This register specifies the length of data (in bytes) to be read or written. The maximum length is 255, while the minimum is 1. When the op_code is RSTART, STOP or END, this value is meaningless.
  
**Footer Information:** 
Espressif Systems
392 ESP32 TRM (Version 5.6)
Submit Documentation Feedback