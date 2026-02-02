**Title:**
Chapter 21 I2C Controller (I2C)

**Subtitle:**
Register 21.10. I2C_INT_ENA_REG (0x0028)

**Menu/Navigation Link:**
GoBack

**Body Text with List of Interrupt Enable Bits for the I2C Controller:**

- **I2C_TX_SEND_EMPTY_INT_ENA**: The interrupt enable bit for the `I2C_TX_SEND_EMPTY_INT` interrupt. (R/W)
- **I2C_RX_REC_FULL_INT_ENA**: The interrupt enable bit for the `I2C_RX_REC_FULL_INT` interrupt. (R/W)
- **I2C_ACK_ERR_INT_ENA**: The interrupt enable bit for the `I2C_ACK_ERR_INT` interrupt. (R/W)
- **I2CTrans_START_INT_ENA**: The interrupt enable bit for the `I2CTrans_START_INT` interrupt.
  - **Note:** This is a read/write register.

- **I2C_TIME_OUT_INT_ENA**: The interrupt enable bit for the `I2C_TIME_OUT_INT` interrupt. (R/W)
- **I2CTrans_COMPLETE_INT_ENA**: The interrupt enable bit for the `I2CTrans COMPLETE INT` interrupt.
  - **Note:** This is a read/write register.

- **I2C_MASTER_TRANComp_INT_ENA**: The interrupt enable bit (`I2C_MASTER TRAN COMP INT`) for the `I2C_MASTER TRAN COMP INT` interrupt. (R/W)
- **I2C_ARBITRATION_LOST_INT_ENA**: The interrupt enable bit for the `I2C_ARBITRATION_LOST_INT` interrupt.
  - **Note:** This is a read/write register.

- **I2C_SLAVE_TRANComp_INT_ENA**: The interrupt enable bit (`I2C_SLAVE TRAN COMP INT`) for the `I2C_SLAVE TRAN COMP INT` interrupt. (R/W)
- **I2C_END_DETECT_INT_ENA**: The interrupt enable bit for the `I2C_END DETECT INT` interrupt.
  - **Note:** This is a read/write register.

- **I2C_RXFIFO_OVF_INT_ENA**: The interrupt enable bit (`I2C_RXFIFO OVF INT`) for the `I2C_RXFIFO OVF INT` interrupt. (R/W)
- **I2C_TXFIFO_EMPTY_INT_ENA**: The interrupt enable bit (`I2C_TXFIFO EMPTY INT`) for the `I2C_TXFIFO EMPTY INT` interrupt.
  - **Note:** This is a read/write register.

- **I2C_RXFIFO_FULL_INT_ENA**: The interrupt enable bit (`I2C_RXFIFO FULL INT`) for the `I2C_RXFIFO FULL INT` interrupt. (R/W)

**Footer:**
Espressif Systems
409 ESP32 TRM (Version 5.6)
Submit Documentation Feedback