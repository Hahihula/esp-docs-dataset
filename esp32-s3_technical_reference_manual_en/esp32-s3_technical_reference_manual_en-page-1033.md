**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Back Link:**
GoBack

**Register Information:**
- **Register Name:** Register 27.25. I2C_INT_STATUS_REG (0x002C)
- **Bit Description Table:**
  - Bits are labeled from `31` to `0`.
  - Each bit is associated with a specific interrupt status for the I2C controller.

**Interrupt Status Descriptions:**

- **I2C_RXFIFO_WM_INT_ST (RO)**
  - The masked interrupt status bit for the I2C_RXFIFO_WM_INT interrupt.
  
- **I2C_TXFIFO_WM_INT_ST (RO)**
  - The masked interrupt status bit for the I2C_TXFIFO_WM_INT interrupt.

- **I2C_RXFIFO_OVF_INT_ST (RO)**
  - The masked interrupt status bit for the I2C_RXFIFO_OVF_INT interrupt.
  
- **I2C_END_DETECT_INT_ST (RO)**
  - The masked interrupt status bit for the I2C_END_DETECT_INT interrupt.

- **I2C_BYTETrans_Done_INT_st (The masked interrupt status bit for the I2C_BYTETransDONE_INT interrupt. (RO))**

- **I2C_ARBITRATION_Lost_INT_st (The masked interrupt status bit for the I2C_ARBITRATION_LOST_INT interrupt. (RO))**

- **I2C_MST_TXFIFO_UDF_INT_st (The masked interrupt status bit for the I2C_MST_TXFIFO_UDF_INT interrupt. (RO))**

- **I2C_trans_complete_INT_st (The masked interrupt status bit for the I2C_TRANSComplete_INT interrupt. (RO))**

- **I2C_time_out_INT_st (The masked interrupt status bit for the I2C_TIME_OUT_INT interrupt. (RO))**

- **I2C_trans_start_INT_st (The masked interrupt status bit for the I2CTransStart_INT interrupt. (RO))**

- **I2C_NACK_INT_st (The masked interrupt status bit for the I2C_NACK_INT interrupt. (RO))**

- **I2C_TXFIFO_OVF_INT_st (The masked interrupt status bit for the I2C_TXFIFO_OVF_INT interrupt. (RO))**

- **I2C_RXFIFO_UDF_INT_st (The masked interrupt status bit for the I2C_RXFIFO_UDF_INT interrupt. (RO))**

**Footer:**
Continued on the next page...

**Document Footer Information:**
Espressif Systems
1033 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback