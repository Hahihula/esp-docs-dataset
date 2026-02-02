**Title:**
Chapter 30 Remote Control Peripheral (RMT)

**Subtitles and Sections:**

1. **Register 30.3. RMT_INT_RAW_REG (0x00A0)**
   - Diagram of register bits with labels:
     - `RMT_CHn_TX_THR_EVENT_INT_RAW`: The raw interrupt status bit for the `RMT_CHn_ERR_INT` interrupt.
     - `RMT_CHn_ERR_INT_RAW`: The raw interrupt status bit for the RMT_CHn_ERR_INT RAW (RO).
     - `RMT_CHn_RX_END_INT_RAW`: The raw interrupt status bit for the RMT_CHn_RX_END_INT interrupt.

2. **Register 30.4. RMT_INT_ST_REG (0x00A4)**
   - Diagram of register bits with labels:
     - `RMT_CHn_TX_THR_EVENT_INT`: The masked interrupt status bit for the RMT_CHn_TX_THR_EVENT_INT interrupt.
     - `RMT_CHn_ERR_INT_ST`: The masked interrupt status bit for the RMT_CHn_ERR_INT interrupt (RO).
     - `RMT_CHn_RX_END_INT_ST`: The masked interrupt status bit for the RMT_CHn_RX_END_INT interrupt.

**Footer:**
- Page number 733
- Document version ESP32 TRM (Version 5.6)
- Link to submit documentation feedback

**Note:** 
The text includes descriptions of specific bits in registers related to remote control peripherals, detailing their functions and the type of data they represent or manage within a system context.

**GoBack Button:**
There is an interactive "GoBack" button at the top right corner.