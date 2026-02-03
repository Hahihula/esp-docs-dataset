**Title: Chapter 37 Remote Control Peripheral (RMT)**

**Register Section Title:** Register 37.3, RMT_CHnCONFO_REG (n = 0-3) (0x0020+0x4*n)

**Binary Table Description**
- The table shows a binary representation of the register with various fields labeled.
- Fields include: `RMT_TX_START_CHn`, `RMT_RXStartEn`, etc.

**Field Descriptions and Functions**

1. **RMT_TX_START_CHn (W)**
   - Set this bit to start sending data in channel n.

2. **RMT_MEM_RD_RST_CHn (W)**
   - Set this bit to reset RAM read address accessed by the transmitter of channel n.
   
3. **RMT_APB_MST_RST_CHn (W)**
   - Set this bit to reset RAM W/R address for channel n when accessed by APB FIFO.

4. **RMT_TX_CONTI_MODE_CHn (R/W)**
   - In this mode, the transmitter starts its transmission from the first data.
   - If an end-marker is encountered: The transmitter starts transmitting data again starting with the next block of RAM or continues to transmit until all last data in loops if no end-marker.

5. **RMT_MEM_TX.WRAP_EN_CHn (R/W)**
   - Set this bit to enable wrap TX mode for channel n.
   - In this mode, if the TX data size is larger than the channel's RAM block size: The transmitter continues transmitting until all last data in loops or resets when reaching end-marker.

6. **RMT_IDLE_OUT_LV_CHn (R/W)**
   - This bit configures the level of output signal for channel n.
   - When the transmitter is idle, it determines if an enable-bit should be set to 1: The output state will follow RMT_IDLE_OUT_LV_CHn.

7. **RMT_TX_STOP_CHn (R/W)**
   - Set this bit to stop the transmitter of channel n sending data out.
   
8. **RMT_DIV_CNT_CHn (R/W)**
   - This field is used for configuring divider settings, which affects clock division rate in channel n.

9. **RMT_MEM_SIZE_CHn (R/W)**
   - This field configures maximum number of memory blocks allocated to channel n.
   
**Footer Note:** Continued on the next page...

**Document Footer:**
- Page 1427
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems

**Navigation Links:**
- Submit Documentation Feedback