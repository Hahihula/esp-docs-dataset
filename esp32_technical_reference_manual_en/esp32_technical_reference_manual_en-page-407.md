**Chapter Title:**
Chapter 21 I2C Controller (I2C)

**Register Information:**
- Register Name: 21.8. I2C_INT_RAW_REG (0x0020)
- GoBack link

**Diagram Description:**
A diagram showing the layout of register bits with labels for each bit from `I2C_TX_SEND_EMPTY_INT_RAW` to `I2C_RXFIFO_FULL_INT_RAW`.

**Text Content and Descriptions in Markdown Format:**

1. **I2C_TX_SEND_EMPTY_INT_RAW**: The raw interrupt status bit for the I2C_TX_SEND_EMPTY_INT_raw interrupt.
   - (RO)

2. **I2C_RX_REC_FULL_INT_RAW**: The raw interrupt status bit for the I2C_RX_REC_FULL_INT_raw interrupt.
   - (RO)

3. **I2C_ACK_ERR_INT_RAW**: The raw interrupt status bit for the I2C_ACK_ERR_INT_raw interrupt.
   - (RO)

4. **I2CTrans_START_INT_RAW**: The raw interrupt status bit for the I2CTrans_START_INT_raw interrupt.
   - (RO)

5. **I2C_TIME_OUT_INT_RAW**: The raw interrupt status bit for the I2CTIME_OUT_INT_raw interrupt.
   - (RO)

6. **I2CTrans_COMPLETE_INT_RAW**: The raw interrupt status bit for the I2CTransComplete_INT_raw interrupt.
   - (RO)

7. **I2C_MASTER_TRANComp_INT_RAW**: 
   - Description: The raw interrupt status bit for the I2CMasterTranComp_INT_raw interrupt.

8. **I2C_ARBITRATION_LOST_INT_RAW**:
   - Description: The raw interrupt status bit for the I2CarbIntLost_INT_raw interrupt.
   - (RO)

9. **I2C_SLAVE_TRANComp_INT_RAW**:
   - Description: The raw interrupt status bit for the I2CSlaveTranComp_INT_raw interrupt.

10. **I2C_END_DETECT_INT_RAW**: 
    - Description: The raw interrupt status bit for the I2CEndDetect_INT_raw interrupt.
    - (RO)

11. **I2C_RXFIFO_OVF_INT_RAW**:
    - Description: The raw interrupt status bit for the I2CRXFIFO_OVF_INT_raw interrupt.

12. **I2C_TXFIFO_EMPTY_INT_RAW**: 
    - Description: The raw interrupt status bit for the I2CTXFIFO_EMPTY_INT_raw interrupt.
    - (RO)

13. **I2C_RXFIFO_FULL_INT_RAW**:
    - Description: The raw interrupt status bit for the I2CRXFIFO_FULL_INT_raw interrupt.

**Footer Information:**
- Company Name: Espressif Systems
- Page Number: 407
- Document Title: ESP32 TRM (Version 5.6)
- Submit Documentation Feedback link