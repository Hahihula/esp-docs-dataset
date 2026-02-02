**Title:**
Chapter 21 I2C Controller (I2C)

**Subtitle:**
21.3.6 Master Reads from Slave

**Figure Caption and Description:**
- **Figure 21.3-9:** "Master Reads from Slave with 7-bit Address"
  
  - The figure shows a block diagram of the communication between master and slave in an I2C bus, illustrating various signals such as SCL (clock), SDA (data), cmd0 to cmd4 for command lines, byte_num indicating data length, and RAM addresses.

**Body Text:**
- **Paragraph:** "Figure 21.3-9 shows the Master Reading N-bytes of data from an Slave with a 7-bit address. At first, the Master needs to send the address of the Slave, so cmd1 is a WRITE command. The byte that this command sends is the slave address plus the R/W flag, which in this case is 1 and, therefore, indicates that this is going to be a read operation. The Slave starts to send data to the Master if the addresses match. The Master will return ACK, according to the ack_value in the READ command, upon receiving every byte."

- **Paragraph:** "As can be seen from Figure 21.3-9, READ is divided into two segments. The Master replies ACK to N-1 bytes in cmd2 and does not reply ACK to the single byte READ command in cmd3, i.e., the last transmitted data. Users can configure it as they wish."

- **Paragraph:** "When storing the received data, Master will start from the first address in RAM. Byte0 (Slave address + 1-bit R/W marker bit) will be overwritten."
  
- **Paragraph:** "When the END command is not used, the Master can receive up to (13*255) bytes of valid data. The cmd unit is populated with RSTART + 1 WRITE + 13 READ + 1 STOP."

**Additional Figure Caption and Description:**
- **Figure 21.3-10:** "Master reading data from a slave with a 10-bit address"
  
  - This figure explains how to enable the master mode by setting I2C_SLAVE_ADDR_10BIT_EN bit, preparing RAM for sending two bytes of R/W operation and enabling one transaction using I2C TRANS_START bit.

**Footer:**
- "Espressif Systems ESP32 TRM (Version 5.6)"
- Links to Submit Documentation Feedback