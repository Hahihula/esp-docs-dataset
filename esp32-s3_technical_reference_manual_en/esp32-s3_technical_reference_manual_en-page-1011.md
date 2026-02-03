**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Body Text with List Items and Annotations:**

- Not match: If the received ACK value does not match ack_exp, I2C master generates an `I2C_NACK_INT` (master) interrupt and stops data transfer.

1. **I2C slave receives memory address sent by I2C master** and adds the offset.
2. **I2C master sends a RSTART and the third byte in TX RAM**, which is ((0x78 | `I2C_SLAVE_ADDR`[9:8])«1) and a R bit.

3. **I2C slave repeats step 11**. If its address matches the address sent by I2C master, `I2C_slave` proceed on to the next steps.
4. After `I2C_SLAVE_STRETCH_INT` (slave) is generated, the `I2C_STRETCH_CAUSE` bit is O. The address of `I2C_slave` matches the address sent over SDA, and I2C slave needs to send data.

5. Write data to be sent to TX RAM of `I2C_slave` in either FIFO mode or non-FIFO mode according to Section 27.4.10.
6. Set `I2C_SLAVE_SCL_STRETCH_CLR` (slave) to I to release SCL.
7. **I2C slave sends data**, and I2C master checks ACK value or not according to `ack_check_en` (master) in the READ command.

8. If data to be read by I2C master is larger than 32 bytes, an `I2C_SLAVE_STRETCH_INT` (slave) interrupt will be generated when TX RAM of `I2C_slave` becomes empty. In this way, I2C slave can hold SCL low so that software has more time to read data in TX RAM and read data into RX RAM of I2C master. After software has finished reading, you can set `I2C_SLAVE_STRETCH_INT_CLR` (slave) to 1 to clear interrupt.

9. **After receiving the last byte**, if it is valid:
   - If the slave does not have more data or there are no more bytes in the FIFO buffer of I2C slave.
   - The master will stop transfer once `I2C_NACK_INT` occurs, and set `ack_value` (master) to 1.

**Highlighted Section:**
- **27.5.8**: Read `I2C_slave` with a 7-bit Address in Multiple Command Sequences

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback