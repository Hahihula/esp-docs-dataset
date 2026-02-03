**Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Header:**
Register 3712: RMT_INT_ST_REG (0x0074)

**Binary Register Diagram Description:**
The diagram shows a binary register with various fields labeled, such as "reserved," and specific interrupt status bits for different channels of the remote control peripheral. The labels include:
- RMT_CHn_TX_END_INT_ST
- RMT_CHn_ERR_INT_ST
- RMT_CHn_TX_THR_EVENT_INT
- RMT_CHn_TX_LOOP_INT
- RMT_CHm_RX_END_INT
- RMT_CHm_ERR_INT_ST
- RMT_CHm_RX_THR_EVENT_INT

**Text Descriptions:**
1. **RMT_CHn_TX_END_INT_ST (n = 0-3):** The masked interrupt status bit of RMT_CHn_TX_END_INT.
2. **RMT_CHn_ERR_INT_ST (n = 0-3):** The masked interrupt status bit of RMT_CHn_ERR_INT.
3. **RMT_CHn_TX_THR_EVENT_INT (n = 0-3):** The masked interrupt status bit of the TX THR EVENT INT for each channel n from 0 to 3, stored in register RMT_CHn_TX_THR_EVENT_INT.
4. **RMT_CHn_TX_LOOP_INT (n = 0-3):** The masked interrupt status bit of the TX LOOP INT for each channel n from 0 to 3, stored in register RMT_CHn_TX_LOOP_INT.
5. **RMT_CHm_RX_END_INT (m = 4-7):** The masked interrupt status bit of RX END INT for channels m ranging between 4 and 7, stored in register RMT_CHm_RX_END_INT.
6. **RMT_CHm_ERR_INT_ST (m = 4-7):** The masked interrupt status bit of ERR INT for each channel n from 0 to 3, stored in register RMT_CHm_ERR_INT.
7. **RMT_CHm_RX_THR_EVENT_INT (m = 4-7):** The masked interrupt status bit of RX THR EVENT INT for channels m ranging between 4 and 7, stored in register RMT_CHm_RX_THR_EVENT_INT.
8. **RMT_CH3_DMA_ACCESS_FAIL_INT_ST:** The masked interrupt status bit of DMA ACCESS FAIL INT for channel CH3, stored in register RMT_CH3_DMA_ACCESS_FAIL_INT.
9. **RMT_CH7_DMA_ACCESS_FAIL_INT:** The masked interrupt status bit of DMA ACCESS FAIL INT for channel CH7, stored in register RMT_CH7_DMA_ACCESS_FAIL_INT.

**Footer:**
Espressif Systems
1435 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback