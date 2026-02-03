**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Section Heading:**
27.5.2.1 Introduction

**Diagram Description and Caption:**
- Diagram showing the interaction between a Master and Slave in an I2C communication.
- **Figure Label:** Figure 27.5-2, "I2Cmaster Writing to a Slave with a 10-bit Address"

**Body Text Explanation of Diagram:**
The diagram illustrates how data is transmitted from one device (Master) to another via the SCL and SDA lines in an I2C communication protocol.

**Subsection Heading:**
27.5.2.2 Configuration Example

**Table Description with Headers, Rows, and Content:**

| Command registers | code | ack_value | ack_exp | ack_check_er | byte_num |
|--------------------|------|----------|--------|--------------|---------|
| I2C_COMMANDO       | RSTART  | —        | —      |              |         |
|                    | WRITE |          | 1      |              | N+2     |
|                    | STOP   |          | —      |              |         |

**Body Text:**
- **Step-by-step Configuration Example:** 
  - Set `I2C_MS_MODE` (master) to 1, and `I2C_MS_MODE` (slave) to 0.
  - Write a value of "1" to `I2C_CONF_UPGATE` (master) and `I2C_CONF_UPGATE` (slave) registers for synchronization purposes. 
  - Configure command registers (`I2C_COMMAND1`, `I2C_COMMAND2`) as per the table.
  - Configure slave address in `I2C_SLAVE_ADDR` register to enable a specific I2C slave's communication with master device, and set `I2C_ADDR_10BIT_EN` (slave) bit for enabling ten-bit addressing. 
  - Write data from Master to Slave by setting the first byte of the address (`I2C_slave`) as part of the TX RAM.
  - Start transfer using registers like `I2C_TRANS_START`.

**Footer:**
- "Espressif Systems"
- Page number and document version information:
  - ESP32-S3 TRM (Version 1.7)
  - Submit Documentation Feedback

**Navigation Link:** 
GoBack