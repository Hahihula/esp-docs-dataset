**Title: Chapter 27 I2C Controller (I2C)**

**Section Title:** 
27.5.6 I2Cmaster Reads I2Cslave with a 10-bit Address in One Command Sequence

**Subsection Title and Content:**
27.5.6.1 Introduction
- **Diagram Description**: The diagram shows the interaction between Master (I2Cmaster) and Slave (I2Cslave). It includes command sequences such as RSTSTART, WRITE, READ, STOP with corresponding byte numbers.
  
**Figure Caption:** 
Figure 27.5-6: I2Cmaster Reading I2Cslave with a 10-bit Address

**Body Text Explanation of Figure and Process Description**: The text explains how the figure shows an example where `I2Cmaster` reads data from an I2C slave using 10-bit addressing, unlike traditional 7-bit. It describes that in this method, the WRITE command is formed by two bytes.

**Subsection Title:**
27.5.6.2 Configuration Example

**List of Steps for Configuration Example**: 
1. Set `I2C_MS_MODE` (master) to 1 and `I2C_MS_MODE` (slave) to 0.
2. Recommend setting `I2C_SLAVE_SCL_STRETCH_EN` (slave) to 1, so that SCL can be held low for more processing time when I2Cslave needs to send data; if this bit is not set, software should write the TX RAM before I2Cmaster initiates transfer.
3. Write `I2C_CONF_UPGATE` (master) and `I2C_CONF_UPGATE` (slave) registers in a scenario where `I2C_SLAVE_SCL_STRETCH_EN` (slave) is 1 to synchronize registers.

**Table Description:**
- **Table Caption**: Command registers of I2Cmaster
- The table lists command register names, op_code values for each column (`ack_value`, `ack_exp`, `ack_check_er`, `byte_num`).

**Footer Information:** 
Espressif Systems  
1007  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback