**Title:**
Chapter 30 Remote Control Peripheral (RMT)

**Subtitles and Sections with Descriptions of Registers:**

1. **Register 30.5, RMT_INT_ENA_REG (0x00A8)**
   - Diagram:
     ```
     31 30 29 28 27 26 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1
     RMT_CHn_TX_THR_EVENT_INT_ENA   The interrupt enable bit for the RMT_CHn_ERROR_INT interrupt. (R/W)
     RMT_CHn_ERR_INT_ENA           The interrupt enable bit for the RMT_CHn_ERROR_INT interrupt. (R/W)
     RMT_CHn_RX_END_INT_ENA         The interrupt enable bit for the RMT_CHn_RX_END_INT interrupt. (R/W)
     RMT_CHn_TX_END_INT_ENA         The interrupt enable bit for the RMT_CHn_TX_END_INT interrupt. (R/W)
     ```
   - Description:
     - **RMT_CHn_TX_THR_EVENT_INT_ENA:** The interrupt enable bit.
     - **RMT_CHn_ERR_INT_ENA:** The interrupt enable bit for error interrupts.
     - **RMT_CHn_RX_END_INT_ENA:** The interrupt enable bit for receive end interrupts.
     - **RMT_CHn_TX_END_INT_ENA:** The interrupt enable bit for transmit end interrupts.

2. **Register 30.6, RMT_INT_CLR_REG (0x00AC)**
   - Diagram:
     ```
     31 30 29 28 27 26 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1
     RMT_CHn_TX_THR_EVENT_INT_CLR    Set this bit to clear the RMT_CHn_TX_THR_EVENT_INT interrupt. (WO)
     RMT_CHn_ERR_INT_CLR             Set this bit to clear the RMT_CHn_ERR_INT interrupt. (WO)
     RMT_CHn_RX_END_INT_CLR          Set this bit to clear the RMT_CHn_RX_END_INT interrupt. (WO)
     RMT_CHn_TX_END_INT_CLR          Set this bit to clear the RMT_CHn_TX_END_INT interrupt. (WO)
     ```
   - Description:
     - **RMT_CHn_TX_THR_EVENT_INT_CLR:** Clears transmit event interrupt.
     - **RMT_CHn_ERR_INT_CLR:** Clears error interrupt.
     - **RMT_CHn_RX_END_INT_CLR:** Clears receive end interrupt.
     - **RMT_CHn_TX_END_INT_CLR:** Clears transmit end interrupt.

**Footer:**
- Page number and document version:
  ```
  Espressif Systems
  Submit Documentation Feedback
  ESP32 TRM (Version 5.6)
  ```