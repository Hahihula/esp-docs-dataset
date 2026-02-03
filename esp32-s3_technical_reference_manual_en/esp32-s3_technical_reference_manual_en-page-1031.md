**Title: Chapter 27 I2C Controller (I2C) Register**

**Subtitle: GoBack**

**Register Name:** I2C_INT_CLR_REG (0x0024)

**Bit Description Table:**
- **31**: Reserved

**Bit Positions and Descriptions with Reset Values:**
- Bit positions range from 31 to various lower values.
  
**Descriptions of Each Bit:**
- `I2C_RXFIFO_WM_INT_CLR`: Set this bit to clear the I2C_RXFIFO_WM_INT interrupt. (WT)
- `I2C_TXFIFO_WM_INT_CLR`: Set this bit to clear the I2C_TXFIFO_WM_INT interrupt.
- `I2C_RXFIFO_OVF_INT_CLR`: Set this bit to clear the I2C_RXFIFO_OVF_INT interrupt.
- `I2C_END_DETECT_INT_CLR`: Set this bit to clear the I2C_END_DETECT_INT interrupt. (WT)
- `I2C_BYTETrans_DONE_INT_CLR`: Set this bit to clear the I2C_BYTETransDONE_INT interrupt.

**Additional Interrupts:**
- `I2C_ARBITRATION_LOST_INT_CLR`
- `I2C_MST_TXFIFO_UDF_INT_CLR`
- `I2C_TRANSComplete_INT_CLR`
- `I2C_TIME_OUT_INT_CLR`
- `I2C_TRANS_START_INT_CLR`
- `I2C_NACK_INT_CLR`
- `I2C_TXFIFO_OVF_INT_CLR`
- `I2C_RXFIFO_UDF_INT_CLR`
- `I2C_SCL_ST_TO_INT_CLR`
- `I2C_SCL_MAIN_ST_TO_INT_CLR`
- `I2C_DET_START_INT_CLR`
- `I2C_SLAVE_STRETCH_INT_CLR`
- `I2C_GENERAL_CALL_INT_CLR`

**Footer:**
- "Espressif Systems"
- Document version information (1031 ESP32-S3 TRM [Version 1.7])
- Feedback link ("Submit Documentation Feedback")