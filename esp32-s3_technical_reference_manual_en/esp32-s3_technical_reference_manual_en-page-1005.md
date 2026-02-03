**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**GoBack Link:** GoBack

**Section Heading:**
27.5.5.1 Introduction

**Figure Caption and Description:**
- **Figure 27.5-5**: "I2Cmaster Reading I2Cslave with a 7-bit Address"
- The figure shows the communication between an I2C master (labeled as Master) and an I2C slave (labeled as Slave). It includes two columns labeled 'cmd' for command, 'op_code', 'byte_num', on the left side under "Master" column; corresponding to RAM addresses and byte numbers. The right-side shows a similar structure but with labels like 'addr0', 'addr1', etc., indicating memory locations in I2C slave.

**Body Text:**
- Figure 27.5-5 illustrates how an I2C master reads N bytes of data from an I2C slave using 7-bit addressing.
- The command `cmd1` is a WRITE command, and when this command executes on the bus it sends the address to which the byte sent comprises a 7-bit I2Cslave address. When R/W bit (Read/Write) indicates a READ operation.

**Subsection Heading:**
27.5.5 Configuration Example

**List of Steps in Configuration Example:**
1. Set `I2C_MS_MODE` for master to 1 and slave mode (`I2C_MS_MODE`) set as 0.
2. Recommend setting `I2C_SLAVE_STRETCH_EN` (slave stretch enable) bit, so that SCL can be held low during more processing time when I2Cslave needs data transfer; if this is not done software should write to TX RAM before master initiates the transaction for scenarios where slave is 1.
3. Write `I2C_CONF_UPGATE` (master and slave) registers in sync.
4. Configure command registers of I2Cmaster.

**Table:**
- **Command registers of I2Cmaster**: 
  - ack_value
  - ack_exp
  - ack_check_er
  - byte_num

**Footer Information:**  
Espressif Systems, Document ID (1005), ESP32-S3 TRM (Version 1.7)