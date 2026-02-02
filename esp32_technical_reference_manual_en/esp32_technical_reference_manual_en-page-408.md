**Title:**
Chapter 21 I²C Controller (I²C)

**Subtitle:**
Register 21.9. I²C_INT_CLR_REG (0x0024)

**Menu/Navigation Link:**
GoBack

**Diagram/Table Description:**
A table showing the register bits with labels for each bit position, ranging from 'reserved' to various interrupt clear registers.

**Body Text:**

- **I2C_TX_SEND_EMPTY_INT_CLR**: Set this bit to clear the I²C_TX_SENDEMPTYINT interrupt. (WO)
- **I2C_RX_REC_FULL_INT_CLR**: Set this bit to clear the I²C_RX_RECFULLINT interrupt. (WO)
- **I2C_ACK_ERR_INT_CLR**: Set this bit to clear the I²C_ACK_ERR_INT interrupt. (WO)
- **I2CTrans_START_INT_CLR**: Set this bit to clear the I²CTransSTARTINT interrupt. (WO)
- **I2CTime_OUT_INT_CLR**: Set this bit to clear the I²CTimeOutINT interrupt. (WO)
- **I2CTrans_COMPLETE_INT_CLR**: Set this bit to clear the I²CTransCompleteINT interrupt. (WO)
- **I2C_MASTER_TRAN_COMP_INT_CLR**: Set this bit to clear the I²CMasterTranCompINT interrupt. (WO)
- **I2C_ARBITRATION_LOST_INT_CLR**: Set this bit to clear the I²C_ArbitrationLostINT interrupt. (WO)
- **I2C_SLAVE_TRANComp_INT_CLR**: Set this bit to clear the I²CSlaveTranCompINT interrupt. (WO)
- **I2C_END_DETECT_INT_CLR**: Set this bit to clear the I²CEndDetectINT interrupt. (WO)
- **I2CRXFIFO_OVF_INTECLR**: Set this bit to clear the I²CRXFIFO_OVF_INTECLR interrupt. (WO)
- **I2CTXFIFO_EMPTY_INT_CLR**: Set this bit to clear the I²CTXFIFO_EMPTYINT interrupt. (WO)
- **I2CRXFIFO_FULL_INT_CLR**: Set this bit to clear the I²CRXFIFO_FULLINT interrupt. (WO)

**Footer:**
Espressif Systems
408 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback