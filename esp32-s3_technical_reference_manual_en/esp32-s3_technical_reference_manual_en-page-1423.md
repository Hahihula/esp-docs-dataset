**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Table Header:**
Table 37.3-1 – cont’d from previous page

**Table Content:**

| Register | Bit/Field Configuration Update |
|----------|----------------------------------|
| RMT_CHnCARRIER_DUTY_REG | RMT_TX_CONTI_MODE_CHn |
|                           | RMT_CARRIER_HIGH_CHn |
|                           | RMT_CARRIER_LOW_CHn |
| RMT_CHn_TX_LIM_REG | RMT_TX_LOOP_CNT_EN_CHn |
|                           | RMT_TX_LOOP_NUM_CHn |
|                           | RMT_TX_LIM_CHn |
| RMT_TX_SIM_REG | RMT_TX_SIM_EN |
| RX Channel |                    |
|            | RMT_CARRIER_OUT_LV_CHm |
|            | RMT_CARRIER_EN_CHm |
| RMT_CHmCONFO_REG | RMT_IDLE_THRES_CHm |
|                           | RMT_DIV_CNT_CHm |
|                           | RMT_RX_FILTER_THRES_CHm |
| RMT_CHmCONF1_REG | RMT_RX_EN_CHm |
|                    | RMT_CARRIER_HIGHThRES_CHm |
| RMT_CHn_RX_CARRIER_RM_REG | RMT_CARRIER_LOWThRES_CHm |
|                           | RMT_RX_LIM_CHm |
| RMT_CHn_RX_LIM_REG | RMT_TX_LOOP_NUM |
|                           | RMT_REF_CNT_RST_CHm |

**Section Title:**
37.4 Interrupts

**Body Text:**

- **RMT_CHn/m_ERR_INT:** triggered when channel n/m does not read or write data correctly. For example, the receiver still tries to write data into RAM when the RAM is full. Or the transmitter still tries to read data from RAM when the RAM is empty.
  
- **RMT_CHn_TX_THR_EVENT_INT:** triggered when the amount of data the transmitter has sent matches the value of RMT_CHn_TX_LIM_REG.

- **RMT_CHm_RX_THR_EVENT_INT:** triggered each time when the amount of data received by the receiver reaches the value set in RMT_CHm_RX_LIM_REG.

- **RMT_CHn_TX_END_INT:** triggered when the transmitter has finished transmitting signals.
  
- **RMT_CHm_RX_END_INT:** triggered when the receiver has finished receiving signals.
  
- **RMT_CHn_TX_LOOP_INT:** triggered when the loop counting reaches the value set by RMT_TX_LOOP_NUM in continuous TX mode.

- **RMT_CH3_DMA_ACCESS_FAIL_INT:** triggered when the result of (the entries written to channel 3’s RAM - the entries transmitted by channel 3) is larger than channel 3’s RAM size, but DAM keeps writing data to this channel.
  
- **RMT_CH7_DMA_ACCESS_FAIL_INT:** triggered when the result of (the entries received by channel 7’s RAM - the entries read by DMA) is larger than channel 7’s RAM size, but channel 7 keeps receiving data.

**Footer:**
Espressif Systems
1423 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback