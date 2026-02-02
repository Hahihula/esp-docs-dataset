**Title:**
Chapter 22 I2S Controller (I2S)

**Subtitle:**
Register 22.3. I2S_CONF_REG (0x0008)

**Menu/Navigation Link:**
GoBack

**Table Description with Binary Representation and Labels for Each Bit:**

- **Binary Representation:** 
  - The table shows a binary representation of the register, where each bit is labeled from right to left.

**Register Description List:**

1. **I2S SIG LOOPBACK**
   - Enable signal loopback mode, with transmitter module and receiver module sharing the same WS and BCK signals.
   - (R/W)

2. **I2S_RX_MSB_RIGHT**
   - Set this bit to place right-channel data at the MSB in the receive FIFO.
   - (R/W)

3. **I2S_TX_MSB_RIGHT**
   - Set this bit to place right-channel data at the MSB in the transmit FIFO.
   - (R/W)

4. **I2S_RX_MONO**
   - Set this bit to enable receiver’s mono mode in PCM standard mode.
   - (R/W)

5. **I2S_TX_MONO**
   - Set this bit to enable transmitter's mono mode in PCM standard mode.
   - (R/W)

6. **I2S_RX_SHORT_SYNC**
   - Set this bit to enable receiver in PCM standard mode.
   - (R/W)

7. **I2S_TX_SHORT_SYNC**
   - Set this bit to enable transmitter in PCM standard mode.
   - (R/W)

8. **I2S_RX_MSB_SHIFT**
   - Set this bit to enable receiver in Philips standard mode.
   - (R/W)

9. **I2S_TX_MSB_SHIFT**
   - Set this bit to enable transmitter in Philips standard mode.
   - (R/W)

10. **I2S_RX_RIGHT_FIRST**
    - Set this bit to receive right-channel data first.
    - (R/W)

11. **I2S_TX_RIGHT_FIRST**
    - Set this bit to transmit right-channel data first.
    - (R/W)

12. **I2S_RX_SLAVE_MOD**
    - Set this bit to enable slave receiver mode.
    - (R/W)

13. **I2S_TX_SLAVE_MOD**
    - Set this bit to enable slave transmitter mode.
    - (R/W)

14. **I2S_RX_START**
    - Set this bit to start receiving data.
    - (R/W)

15. **I2S_TX_START**
    - Set this bit to start transmitting data.
    - (R/W)

16. **I2S_RX_FIFO_RESET**
    - Set this bit to reset the receive FIFO.
    - (R/W)

17. **I2S_TX_FIFO_RESET**
    - Set this bit to reset the transmit FIFO.
    - (R/W)

18. **I2S_RX_RESET**
    - Set this bit to reset the receiver.
    - (R/W)

19. **I2S_TX_RESET**
    - Set this bit to reset the transmitter.
    - (R/W)

**Footer:**

- Page number and document version:
  - "433 ESP32 TRM (Version 5.6)"
  
- Company name:
  - Espressif Systems

- Links for additional actions:
  - Submit Documentation Feedback