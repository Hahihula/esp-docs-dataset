**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Register Information:**
- **Register Name:** TWAI_INT_RAW_REG (0x000C)
- **Binary Representation Diagram**: A binary diagram showing the register bits from bit 31 to bit 0.

**Interrupt Descriptions and Bit Positions in Binary Diagrams:**

1. **TWAI_RX_INT_ST - Receive interrupt**
   - Description: If this bit is set to 1, it indicates there are messages to be handled in the RX FIFO.
   - Access Type (RO): Read Only

2. **TWAI_TX_INT_ST - Transmit interrupt**
   - Description: If this bit is set to 1, it indicates the message transmitting mission is finished and a new transmission is able to execute.
   - Access Type (RO): Read Only

3. **TWAI_ERR_WARN_INT_ST - Error warning interrupt**
   - Description: If this bit is set to 1, it indicates the error status signal and the bus-off status signal of Status register have changed or from 0 to 1.
   - Access Type (RO): Read Only

4. **TWAI_OVERRUN_INT_ST - Data overrun interrupt**
   - Description: If this bit is set to 1, it indicates the data in the RX FIFO is invalid.
   - Access Type (RO): Read Only

5. **TWAI_ERR_PASSIVE_INT_ST - Error passive interrupt**
   - Description: If this bit is set to 1, it indicates the TWAI Controller is switched between error active status and error passive status due to the change of error counters.
   - Access Type (RO): Read Only

6. **TWAI_ARB_LOST_INT_ST - Arbitration lost interrupt**
   - Description: If this bit is set to 1, it indicates an arbitration lost interrupt is generated.
   - Access Type (RO): Read Only

7. **TWAI_BUS_ERR_INT_ST - Error interrupt**
   - Description: If this bit is set to 1, it indicates an error is detected on the bus.
   - Access Type (RO): Read Only

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Link for Feedback:
  - ESP32 TRM (Version 5.6)
  - Submit Documentation Feedback