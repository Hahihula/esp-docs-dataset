**Title:**
Chapter 22 I2S Controller (I2S)

**Subtitle:**
Register 22.7. I2S_INT_CLR_REG (0x0018)

**Diagram Description:**
The diagram shows a register layout with various bits labeled for different interrupt clear functions related to the I2S controller.

**Body Text and Table:**

- **I2S_OUT_TOTAL_EOF_INT_CLR**: Set this bit to clear the `I2S_OUT_TOTAL_EOF_INT` interrupt. (WO)
- **I2S_IN_DSCR_EMPTY_INT_CLR**: Set this bit to clear the `I2S_IN_DSCR_EMPTY_INT` interrupt. (WO)
- **I2S_OUT_DSCR_ERR_INT_CLR**: Set this bit to clear the `I2S_OUT_DSCR_ERR_INT` interrupt. (WO)
- **I2S_IN_DSCR_ERR_INT_CLR**: Set this bit to clear the `I2S_IN_DSCR_ERR_INT` interrupt. (WO)
- **I2S_OUT_EOF_INT_CLR**: Set this bit to clear the `I2S_OUT_EOF_INT` interrupt. (WO)
- **I2S_OUT_DONE_INT_CLR**: Set this bit to clear the `I2S_OUT_DONE_INT` interrupt. (WO)
- **I2S_IN_SUC_EOF_INT_CLR**: Set this bit to clear the `I2S_IN_SUC_EOF_INT` interrupt. (WO)
- **I2S_IN_DONE_INT_CLR**: Set this bit to clear the `I2S_IN_DONE_INT` interrupt. (WO)
- **I2S_TX_HUNG_INT_CLR**: Set this bit to clear the `I2S_TX_HUNG_INT` interrupt. (WO)
- **I2S_RX_HUNG_INT_CLR**: Set this bit to clear the `I2S_RX_HUNG_INT` interrupt. (WO)
- **I2S_TX_REMPTY_INT_CLR**: Set this bit to clear the `I2S_TX_REMPTY_INT` interrupt. (WO)
- **I2S_TX_WFULL_INT_CLR**: Set this bit to clear the `I2S_TX_WFULL_INT` interrupt. (WO)
- **I2S_RX_REMPTY_INT_CLR**: Set this bit to clear the `I2S_RX_REMPTY_INT` interrupt. (WO)
- **I2S_RX_WFULL_INT_CLR**: Set this bit to clear the `I2S_RX_WFULL_INT` interrupt. (WO)
- **I2S_TX_PUT_DATA_INT_CLR**: Set this bit to clear the `I2S_TX_PUT_DATA_INT` interrupt. (WO)
- **I2S_RX_TAKE_DATA_INT_CLR**: Set this bit to clear the `I2S_RX_TAKE_DATA_INT` interrupt. (WO)

**Footer:**
Espressif Systems
437 ESP32 TRM (Version 5.6)