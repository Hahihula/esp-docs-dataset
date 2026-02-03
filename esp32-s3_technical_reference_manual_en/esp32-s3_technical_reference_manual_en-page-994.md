**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Section with List and Descriptions of Register Bits:**

3. **ack_value:** Used to configure the level of the ACK bit sent by the I2C controller during a read operation.
   - This bit is ignored in RSTART, STOP, END, and WRITE conditions.

4. **ack_exp:** Used to configure the level of the ACK bit expected by the I2C controller during a write operation.
   - This bit is ignored during RSTART, STOP, END, and READ conditions.

5. **ack_check_en:** Used to enable the I2C controller during a write operation to check whether the ACK level sent by the slave matches ack_exp in the command.
   - If this bit is set and the level received does not match ack_exp in the WRITE command, the master will generate an I2C_NACK_INT interrupt and a STOP condition for data transfer. 
   - If this bit is cleared, the controller will not check the ACK level sent by the slave.

6. **byte_num:** Specifies the length of data (in bytes) to be read or written.
   - This bit can range from 1 to 255 bytes and it's ignored during RSTART, STOP, and END conditions.

**Explanation:**
Each command sequence is executed starting from command register O and terminated by a STOP or an END. Therefore, there must be a STOP or an END command in the eight command registers.
- A complete data transfer on the I2C bus should be initiated by a START and terminated by a STOP. The transfer process may be completed using multiple sequences, separated by END commands.

**Subsection Title:**
27.4.10 TX/RX RAM Data Storage

**Body Text with Explanation of RAM Modes:**

Both TX RAM and RX RAM are 32 x 8 bits, and can be accessed in FIFO or non-FIFO mode.
- If I2C_NONFIFO_EN bit is cleared, both RAMs are accessed in FIFO mode; if I2C_NONFIFO_EN bit is set, both RAMs are accessed in non-FIFO mode.

TX RAM stores data that the I2C controller needs to send. During communication:
- When the I2C controller reads from TX RAM and sends them sequentially via SDA.
- In master mode all data must be stored in TX RAM; when working with slave addresses, read/write bits are sent first followed by slave address.

RX RAM stores received during communication: 
- CPU can only access RX RAM either directly or indirectly through I2C_DATA_REG. 

**Additional Information about Accessing RAMs:****

TX RAM:
- Can be accessed in FIFO mode (directly) and non-FIFO direct addressing.
- In FIFO, the address is incremented automatically by hardware.

RX RAM: 
- CPU can only read RX RAM via fixed addresses or directly from I2C_DATA_REG. 

**Footer Information:**
Espressif Systems
994 ESP32-S3 TRM (Version 1.7)