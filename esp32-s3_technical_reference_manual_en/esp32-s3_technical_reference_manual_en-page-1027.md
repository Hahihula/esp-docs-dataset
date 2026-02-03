**Title: Chapter 27 I2C Controller (I2C)**

**Register Name and Address:** Register 27.19, I2C_SR_REG (0x0008)

---

### Table of Registers:
- **I2C_SOL_STATE_LAST**
- **I2C_MAIN_STATE LAST**
- **I2C_TXIFO_CNT**
- **I2C_STRETCH_CAUSE**
- **I2C_RXFIFO_CNT**
- **I2C RESP_REC**

**Field Descriptions:**

1. **I2C RESP_REC:** The received ACK value in master mode or slave mode.
   - 0: ACK
   - 1: NACK (Read/Write)

2. **I2C_SLAVE_RW:** When in slave mode, the behavior of data transfer:
   - 0: Master writes to slave; 
   - 1: Master reads from slave

3. **I2C_ARB_LOST:** Indicates when I2C controller loses control over SCL line.
   - Changes bit value changes to 1 (Read/Write)

4. **I2C BUS BUSY:** Indicates the status of bus activity:
   - 0: Bus is idle
   - 1: Bus busy transferring data

5. **I2C_SLAVE_ADDRESSED:** When in slave mode, indicates if address sent by master matches.
   - Bit value at high level (Read/Write)

6. **I2C_RXFIFO_CNT:** Represents the number of byte data to be sent.

7. **I2C_STRETCH_CAUSE:** Indicates cause for SCL clock stretching:
   - 0: Stretching low when master starts reading
   - 1: Stretching high in slave mode

8. **I2C_TXFIFO_CNT:** Stores the number of data bytes received from RAM.

9. **I2C_SCL_MAIN_STATE LAST:** Indicates status machine state.
   - 0: Idle; 
   - 1: Address shift;
   - 2: ACK address
   - 3: Receive data
   - 4: Transmit data
   - 5: Send ACK
   - 6: Wait for ACK

10. **I2C_SCL_STATE LAST:** Indicates the status of state machine used to produce SCL.
    - 0: Idle;
    - 1: Start; 
    - 2: Falling edge; 
    - 3: Low; 
    - 4: Rising edge
    - 5: High; 
    - 6: Stop

---

**Footer:**  
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)