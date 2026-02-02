**Title:**
Chapter 22 I2S Controller (I2S) Register

**Subtitle:**
Register 22.8. I2S_TIMING_REG (0x001c)

**Binary Diagram Description:**
The diagram shows a binary register with various fields labeled as follows:
- `I2S_TX_BCK_IN_INV`
- `I2S_DATA_ENABLE_DELAY`
- `I2S_RX_DSYNC_SW`
- `I2S_TX_SD_OUT_DELAY`
- `I2S_TX_WS_OUT_DELAY`
- And others...

**Field Descriptions:**
1. **I2S_TX_BCK_IN_INV**: Set this bit to invert the BCK signal into the slave transmitter.
   - (R/W)
   
2. **I2S_DATA_ENABLE_DELAY**: Number of delay cycles for data valid flag.
   - (R/W)
   
3. **I2S_RX_DSYNC_SW**: Set this bit to synchronize signals into the receiver in double sync method.
   - (R/W)
   
4. **I2S_TX_DSYNC_SW**: Set this bit to synchronize signals into the transmitter in double sync method.
   - (R/W)
   
5. **I2S_RX_BCK_OUT_DELAY**: Number of delay cycles for BCK signal out of the receiver.
   - (R/W)
   
6. **I2S_RX_WS_OUT_DELAY**: Number of delay cycles for WS signal out of the receiver.
   - (R/W)
   
7. **I2S_TX_SD_OUT_DELAY**: Number of delay cycles for SD signal out of the transmitter.
   - (R/W)
   
8. **I2S_TX_WS_OUT_DELAY**: Number of delay cycles for WS signal out of the transmitter.
   - (R/W)
   
9. **I2S_TX_BCK_OUT_DELAY**: Number of delay cycles for BCK signal out of the transmitter.
   - (R/W)
   
10. **I2S_RX_SD_IN_DELAY**: Number of delay cycles for SD signal into the receiver.
    - (R/W)
    
11. **I2S_RX_WS_IN_DELAY**: Number of delay cycles for WS signal into the receiver.
    - (R/W)
    
12. **I2S_TX_WS_IN_DELAY**: Number of delay cycles for WS signal into the transmitter.
    - (R/W)
    
13. **I2S_TX_BCK_IN_DELAY**: Number of delay cycles for BCK signal into the transmitter.
    - (R/W)

**Footer:**
Espressif Systems
438 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback