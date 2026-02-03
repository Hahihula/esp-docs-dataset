**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Register Information:**
- Register Address: 27.22.
- Register Name: I2C_INT_RAW_REG (0x0020)
- Description of the register contents:
  - The raw interrupt bit for various interrupts related to different functions in an I2C controller.

**Interrupt Bits and Their Functions:**

1. **I2C_RXFIFO_WM_INT_RAW**
   - Function: Raw interrupt bit for the `I2C_RXFIFO_WM_INT` interrupt.
   - Access Mode(s): R/SS/WTC

2. **I2C_TXFIFO_WM_INT_RAW**
   - Function: Raw interrupt bit for the `I2C_TXFIFO_WM_INT` interrupt.
   - Access Mode(s): R/SS/WTC

3. **I2C_RXFIFO_OVF_INT_RAW**
   - Function: Raw interrupt bit for the `I2C_RXFIFO_OVF_INT` interrupt.
   - Access Mode(s): R/SS/WTC

4. **I2C_END_DETECT_INT_RAW**
   - Function: Raw interrupt bit for the `I2C_END_DETECT_INT` interrupt.
   - Access Mode(s): R/SS/WTC

5. **I2C_BYTETrans_DONE_INT_RAW**
   - Function: Raw interrupt bit for the `I2CBYTETransDONE_INT` interrupt.
   - Access Mode(s): R/SS/WTC

6. **I2C_ARBITRATION_LOST_INT_RAW**
   - Function: Raw interrupt bit for the `I2C_ARBITRATION_LOST_INT` interrupt.
   - Access Mode(s): R/SS/WTC

7. **I2C_MST_TXFIFO_UDF_INT_RAW**
   - Function: Raw interrupt bit for the `I2CMST_TXFIFO_UDF_INT` interrupt.
   - Access Mode(s): R/SS/WTC

8. **I2CTransComplete_INT_RAW**
   - Function: Raw interrupt bit for the `I2CTransComplete_INT` interrupt.
   - Access Mode(s): R/SS/WTC

9. **I2C_TIME_OUT_INT_RAW**
   - Function: Raw interrupt bit for the `I2CTIME_OUT_INT` interrupt.
   - Access Mode(s): R/SS/WTC

10. **I2CTransStart_INT_RAW**
    - Function: Raw interrupt bit for the `I2CTRANS_START_INT` interrupt.
    - Access Mode(s): R/SS/WTC

11. **I2C_NACK_INT_RAW**
    - Function: Raw interrupt bit for the `I2CNACK_INT` interrupt.
    - Access Mode(s): R/SS/WTC

12. **I2C_TXFIFO_OVF_INT_RAW**
    - Function: Raw interrupt bit for the `I2CTXFIFO_OVF_INT` interrupt.
    - Access Mode(s): R/SS/WTC

13. **I2C_RXFIFO_UDF_INT_RAW**
    - Function: Raw interrupt bit for the `I2CRX FIFO UDF INT` interrupt.
    - Access Mode(s): R/SS/WTC

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Link:
  - ESP32-S3 TRM (Version 1.7)
  - Submit Documentation Feedback