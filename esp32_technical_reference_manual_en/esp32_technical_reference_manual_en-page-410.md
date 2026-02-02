**Title:**
Chapter 21 I2C Controller (I2C)

**Back to Top Button:**
GoBack

**Register Information Title:**
Register 21.11. I2C_INT_STATUS_REG (0x002c)

**Binary Diagram Description with Labels and Values for Each Bit:**
- The diagram shows a binary representation of the register, labeled from bit positions 31 to bits in sequence down.
- Bits are numbered starting at position 31 on the left side.

**Register Description Table:**

| Register Name | Description |
|---------------|-------------|
| I2C_TX_SEND_EMPTY_INT_ST (RO) | The masked interrupt status bit for the I2C_TX_SEND_EMPTY_INT interrupt. |
| I2C_RX_REC_FULL_INT_ST (RO) | The masked interrupt status bit for the I2C_RX_REC_FULL_INT interrupt. |
| I2C_ACK_ERR_INT_ST (RO) | The masked interrupt status bit for the I2C_ACK_ERR_INT interrupt. |
| I2CTrans_START_INT_ST (RO) | The masked interrupt status bit for the I2CTrans_START_INT interrupt. |
| I2C_TIME_OUT_INT_ST (RO) | The masked interrupt status bit for the I2CTIME_OUT_INT interrupt. |
| I2C_TRANS_COMPLETE_INT_ST (RO) | The masked interrupt status bit for the I2CTRANSComplete_INT interrupt. |
| I2C_MASTER_TRAN COMP_INT_ST (RO) | The masked interrupt status bit for the I2CMasterTransComp_INT interrupt. |
| I2C_ARBITRATION_LOST_INT_ST (RO) | The masked interrupt status bit for the I2CarbitrationLost_INT interrupt. |
| I2C_SLAVE_TRAN COMP_INT_ST (RO) | The masked interrupt status bit for the I2CSlaveTransComp_INT interrupt. |
| I2C_END_DETECT_INT_ST (RO) | The masked interrupt status bit for the I2CEndDetect_INT interrupt. |
| I2C_RXFIFO_OVF_INT_ST (RO) | The masked interrupt status bit for the I2CRXFIFO_OVF_INT interrupt. |
| I2C_TXFIFO_EMPTY_INT_ST (RO) | The masked interrupt status bit for the I2CTXFIFO_EMPTY_INT interrupt. |
| I2C_RXFIFO_FULL_INT_ST (RO) | The masked interrupt status bit for the I2CRXFIFO_FULL_INT interrupt.

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information at Bottom Right Corner:**  
ESP32 TRM (Version 5.6)

(Note: "Reset" is labeled on a specific position in the binary diagram, but it's not part of any register description.)