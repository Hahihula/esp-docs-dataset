**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**GoBack Link:** [GoBack](#)

---

### Section Header:
- **I2S_TX_SLAVE_MOD**

  - *0:* master TX mode

  - *1:* slave TX mode

---

### Section Header:
- **I2S_RX_SLAVE_MOD**

  - *0:* master RX mode

  - *1:* slave RX mode

---

**Subsection Title:**
28.8.1 Master/Slave TX Mode

**Body Text:**
- I2Sn works as a master transmitter:

  - Set the bit `I2S_TX_START` to start transmitting data.

  - TX unit keeps driving the clock signal and serial data.
    - If `I2S_TX_END` is set and all the data in FIFO is transmitted, the master stops transmitting data.
    - If `I2S_TX_END` is cleared and all the data in FIFO is transmitted, meanwhile no new data is filled into FIFO, then the TX unit keeps sending the last data frame.

  - Master stops sending data when the bit `I2S_TX_START` is cleared.

- I2Sn works as a slave transmitter:

  - Set the bit `I2S_TX_START`.

  - Wait for the master BCK clock to enable a transmit operation.
    - If `I2S_TX_END` is set and all the data in FIFO is transmitted, then the slave keeps sending zeros, till the master stops providing BCK signal.

  - If `I2S_TX_END` is cleared and all the data in FIFO is transmitted, meanwhile no new data is filled into FIFO, then the TX unit keeps sending the last data frame.
    - If `I2S_START` is cleared, slave keeps sending zeros till the master stops providing BCK clock signal.

---

**Subsection Title:**
28.8.2 Master/Slave RX Mode

**Body Text:**
- I2Sn works as a master receiver:

  - Set the bit `I2S_RX_START` to start receiving data.
    - RX unit keeps outputting clock signal and sampling input data.

  - RX unit stops receiving data when the bit `I2S_RX_END` is cleared.

- I2Sn works as a slave receiver:
  
  - Set the bit `I2S_RX_START`.

  - Wait for master BCK signal to start receiving data.
    - RX unit stops receiving data when the bit `I2S_RX_END` is cleared. 

---

**Footer:**
Espressif Systems
1047 ESP32-S3 TRM (Version 1.7)

**Link:** [Submit Documentation Feedback](#)